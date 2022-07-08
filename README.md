# genomics-solutionset

*/
wget https://www.niehs.nih.gov/research/resources/assets/docs/artbinmountrainier2016.06.05linux64.tgz
chmod +x artbinmountrainier2016.06.05linux64.tgz
tar -xf artbinmountrainier2016.06.05linux64.tgz
mkdir /mnt/ncsagenomicsstore/input/39_GRCh38.p13
gunzip -d /mnt/datasetreferencegenomes-secondary/dataset/vertebrate_mammalian/Homo_sapiens/latest_assembly_versions/GCF_000001405.39_GRCh38.p13/GCF_000001405.39_GRCh38.p13_genomic.fna.gz -c /mnt/ncsagenomicsstore/input/39_GRCh38.p13/ > /mnt/ncsagenomicsstore/input/39_GRCh38.p13/39_GRCh38.p13_genomic.fasta
mkdir /mnt/ncsagenomicsstore/dataset/simrun01 ; mkdir /simdata
cd /simdata/
nohup ~/art_bin_MountRainier/art_illumina -ss HS25 -sam -i /mnt/ncsagenomicsstore/input/39_GRCh38.p13/39_GRCh38.p13_genomic.fasta -p -l 150 -f 20 -m 200 -s 10 -o paired_dat > nohup2.out 2>&1 &
*/
