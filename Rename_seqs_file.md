

#wkdir
```
/Users/pengfeiliu/A_TBP/B研究生科研/吴丹娜-2021硕士/all纯菌序列wudn_2023.10.13

rename 's/oldstring/newtext/' file00*

for file in file00*; do new=${file/oldstring/newtext}; mv —- "$file" "$new"; done

find . -type f -name 'Lucky-*' | while read FILE ; do
    newfile="$(echo ${FILE} |sed -e 's/\\#U00a9/safe/')" ;
    mv "${FILE}" "${newfile}" ;
done

find . -name '*jpg' -exec bash -c ' mv $0 ${0/\#U00a9NBC/safeNBC}' {} \;

```


#rename and change seq to fasta and merge
```
find . -name '*seq' -exec bash -c ' mv $0 ${0/\(/}' {} \;
find . -name '*seq' -exec bash -c ' mv $0 ${0/\)/}' {} \;

#find . -name '*.txt' -exec bash -c ' mv $0 ${0/\(/}' {} \;

#查看序列数目
 ls *seq|wc -l

#查看文件异常内容
grep '>' *.seq |wc -l

#查看文件异常内容
grep 'Created' *.seq

#add file name to >
#rename
for file in *seq
do
#sed Created: Monday, September 04, 2023 03:20 PM
#^^
sed -e "s/>/>"${file%.*}"/g" "${file}" > "${file%.*}".fna
done

```

#湖水净
```

```

#湖水总
```
cd 湖水总

#AMC
cat *fna > AMC_total_16SrRNA_iso.fasta
grep -c '>' AMC_total_16SrRNA_iso.fasta
76


rm *seq
rm *fna

#YZYC
cat *fna > YZYC_total_16SrRNA_iso.fasta
grep -c '>' YZYC_total_16SrRNA_iso.fasta
205

rm *seq
rm *fna

cat AMC_total_16SrRNA_iso.fasta YZYC_total_16SrRNA_iso.fasta >AMC_YYZC_total_16SrRNA_iso.fasta
```

#重复部分
```


```
