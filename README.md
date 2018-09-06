# VCF-descriptions
Description of VCF fields for different variant-callers
<br>
Platypus. See more at: http://www.well.ox.ac.uk/platypus
<br>
# Example of a multiple-sample VCF (5 samples; adapted from a 45-samples original VCF)<br>
--------------------------------------------<br>
#CHR	POS	ID	REF	ALT	QUAL	FILTER	INFO	FORMAT	sample1	sample2	sample3	sample4	sample5	etc.<br>
chr1	93257374	.	A	G	936.64	PASS	AC=79;AN=90;BRF=0.0;FR=1.0000;HP=1;HapScore=2;MGOF=8;MMLQ=41;MQ=60.0;NF=0;NR=12;PP=457;QD=40.9809343789;SC=AAATTTATGTAGCTTTTATTA;SF=0,1,2,3,4,5,etc.;SbPval=1.0;Source=File;TC=14;TCF=0;TCR=14;TR=12;WE=93257382;WS=93257364	GT:GL:GQ:GOF:NR:NV	1/1:-49.2,-3.31,0.0:33:8:14:12	0/1:-68.72,0.0,-55.72:99:31:39:21	0/1:-49.9,0.0,-36.6:99:23:31:16	1/1:-102.5,-7.5,0.0:75:12:26:26	1/1:-233.6,-17.71,0.0:99:12:60:60	etc.<br>
<br>
AC=79, Allele count in genotypes.<br>
AN=90, Total number of alleles in called genotypes.<br>
BRF=0.0, Fraction of reads around this variant that failed filters.<br>
FR=1.0000, Estimated population frequency of variant.<br>
HP=1, Homopolymer run length around variant locus.<br>
HapScore=2, Haplotype score measuring the number of haplotypes the variant is segregating into in a window.<br>
MGOF=8, Worst goodness-of-fit value reported across all samples.<br>
MMLQ=41, Median minimum base quality for bases around variant.<br>
MQ=60.0, RMS Mapping Quality.<br>
NF=0, Total number of forward reads containing this variant.<br>
NR=12, Total number of reverse reads containing this variant.<br>
FS, Fisher's exact test for strand bias (Phred scale).<br>
PP=457, Posterior probability (phred scaled) that this variant segregates.<br>
QD=40.9809343789, Variant-quality/read-depth for this variant.<br>
SC=AAATTTATGTAGCTTTTATTA, Genomic sequence 10 bases either side of variant position.<br>
SF=0,1,2,3,4,5,etc. (index to sourceFiles, f when filtered).
SbPval=1.0,Binomial P-value for strand bias test.<br>
Source=File<br>
TC=14, Total coverage at this locus.<br>
TCF=0, Total forward strand coverage at this locus.<br>
TCR=14, Total reverse strand coverage at this locus.<br>
TR=12, Total number of reads containing this variant.<br>
WE=93257382, End position of calling window.<br>
WS=93257364, Starting position of calling window.<br>
<br>
<br>
# FILTER field description<br>
GOF=Variant fails goodness-of-fit test.<br>
HapScore=Too many haplotypes are supported by the data in this region.<br>
MQ=Root-mean-square mapping quality across calling region is low.<br>
Q20=Variant quality is below 20.<br>
QD=Variants fail quality/depth filter.<br>
QualDepth=Variant quality/Read depth ratio is low.<br>
REFCALL=This line represents a homozygous reference call<br>
SC=Variants fail sequence-context filter. Surrounding sequence is low-complexity.<br>
alleleBias=Variant frequency is lower than expected for het.<br>
badReads=Variant supported only by reads with low quality bases close to variant position, and not present on both strands.<br>
hp10=Flanking sequence contains homopolymer of length 10 or greater.<br>
strandBias=Variant fails strand-bias filter.<br>
<br>
<br>
# INFO field description<br>
AC=Allele count in genotypes.<br>
AN=Total number of alleles in called genotypes.<br>
BRF=Fraction of reads around this variant that failed filters.<br>
END=Stop position of the interval.<br>
FR=Estimated population frequency of varian.t<br>
FS=Fisher's exact test for strand bias (Phred scale).<br>
HP=Homopolymer run length around variant locus.<br>
HapScore=Haplotype score measuring the number of haplotypes the variant is segregating into in a window.<br>
MGOF=Worst goodness-of-fit value reported across all samples.<br>
MMLQ=Median minimum base quality for bases around variant.<br>
MQ=RMS Mapping Quality.<br>
NF=Total number of forward reads containing this variant.<br>
NR=Total number of reverse reads containing this variant.<br>
PP=Posterior probability (phred scaled) that this variant segregates.<br>
QD=Variant-quality/read-depth for this variant.<br>
ReadPosRankSum=Mann-Whitney Rank sum test for difference between in positions of variants in reads from ref and alt.<br>
SC=Genomic sequence 10 bases either side of variant position.<br>
SF=Source File (index to sourceFiles, f when filtered).<br>
START=Start position of reference call block.<br>
SbPval=Binomial P-value for strand bias test.<br>
Size=Size of reference call block.<br>
Source=Was this variant suggested by Playtypus, Assembler, or from a VCF?.<br>
TC=Total coverage at this locus.<br>
TCF=Total forward strand coverage at this locus.<br>
TCR=Total reverse strand coverage at this locus.<br>
TR=Total number of reads containing this variant.<br>
WE=End position of calling window.<br>
WS=Starting position of calling window.<br>
<br>
<br>
# FORMAT field description<br>
GL=Genotype log10-likelihoods for AA,AB and BB genotypes, where A = ref and B = variant. Only applicable for bi-allelic sites.<br>
GOF=Goodness of fit value.<br>
GQ=Genotype Quality.<br>
GT=Unphased genotypes.<br>
NR=Number of reads covering variant location in this sample.<br>
NV=Number of reads containing variant in this sample.<br>
PL=Normalized, Phred-scaled likelihoods for genotypes as defined in the VCF specification.<br>
<br>
<br>
