#

#seqkit + fastANI
```
seqkit split -i try.fna

cd /Users/pengfeiliu/A_TBP/B研究生科研/吴丹娜-2021硕士/all纯菌序列wudn_2023.10.13

#AMC
AMC_total_16SrRNA_iso.fasta
seqkit split -i AMC_total_16SrRNA_iso.fasta
cd AMC_total_16SrRNA_iso.fasta.split
ls -1 *.fasta > genome.list

#https://github.com/ParBLiSS/FastANI
fastANI --ql genome.list --rl genome.list --fragLen 100 -o AMC_total_16SrRNA_iso_ani.txt

fastANI --ql genome.list --rl genome.list --fragLen 50 -o AMC_total_16SrRNA_iso_anif50.txt


#ALL
seqkit split -i AMC_YYZC_total_16SrRNA_iso.fasta
cd AMC_YYZC_total_16SrRNA_iso.fasta.split
ls -1 *.fasta > genome.list

#https://github.com/ParBLiSS/FastANI
fastANI --ql genome.list --rl genome.list --fragLen 100 -o AMC_YYZC_total_16SrRNA_iso_ani.txt


$ ./fastANI -q B_quintana.fna -r B_henselae.fna --visualize -o fastani.out
$ Rscript scripts/visualize.R B_quintana.fna B_henselae.fna fastani.out.visual
```

#whole genome
```
#https://blog.csdn.net/songyi10/article/details/118378233
从上可以看出，ANI>95%可以明显的分出物种的“种”级别；而AAI在60%是“属”的分界线，90%为“种“的分界线。



```


#ezbiocloud.net/tools/ani
```
#https://www.ezbiocloud.net/tools/ani

```
