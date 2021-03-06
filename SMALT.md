#SMALT 

  SMALT is a pairwise sequence alignment program for the efficient mapping of DNA sequencing reads onto genomic reference sequences. It uses a combination of short-word hashing and dynamic programming. Most types of sequencing platforms are supported including paired-end sequencing reads.
  
  http://wiki.hpc.ufl.edu/doc/SMALT

##Overview

  Running SMALT involves two steps. First, an index of short words has to be built (smalt index). Then the sequencing reads are mapped onto the reference (smalt map).

  SMALT uses a hash table of words of fixed-length sampled along the ge- nomic reference sequence in the file REFSEQ-FILE at equidistant steps. The sequencing reads in the file READ-FILE (and MATE-FILE) are then mapped against the genomic reference sequences one-by-one.

  First, exactly matching seeds are identified in the reference sequences by looking up the k-mer words of the read in the hash index. Based on these seeds, potentially matching sequence segments are selected for alignment by a Smith-Waterman algorithm.

  The reference sequence file REFSEQ-FILE has to be in FASTA or FASTQ format. The sequencing read file READ-FILE can be in FASTA/FASTQ (default) or in SAM/BAM format.

