#CD-hit

#on my mac
#在种（97%）的水平对16S rRNA全长进行聚类，获得有多少个unique 种，并且拿到代表序列
```
cd /Users/pengfeiliu/A_TBP/B研究生科研/吴丹娜-2021硕士/all纯菌序列wudn_2023.10.13/湖水总

#统计序列
AMC_YYZC_total_16SrRNA_iso.fasta
grep -c '>' AMC_YYZC_total_16SrRNA_iso.fasta
281

#read this
#https://sites.google.com/view/cd-hit
#https://github.com/weizhongli/cdhit/wiki

#====== CD-HIT version 4.8.1 (built on Oct 26 2019) ======

#cd hit
conda activate cdhit
cd-hit -i AMC_YYZC_total_16SrRNA_iso.fasta -c 0.97 -T 4 -o AMC_YYZC_total_16SrRNA_iso_cdhit97.fasta -n 5

#281  finished         22  clusters
#在97%水平，只有22个物种


cd-hit -i AMC_YYZC_total_16SrRNA_iso.fasta -c 0.99 -T 4 -o AMC_YYZC_total_16SrRNA_iso_cdhit99.fasta -n 5

281  finished         88  clusters
#在99%水平，只有88个 strain
#100%  281  finished        281  clusters

cd-hit -i AMC_YYZC_total_16SrRNA_iso.fasta -c 0.945 -T 4 -o AMC_YYZC_total_16SrRNA_iso_cdhit94.5.fasta -n 5

#281  finished         11  clusters


```

#同理，也可以在属的水平（94.5%）进行聚类

#usearch: uclust also can do same work，and faster
```


```



#next, blast to find reference
```


```
