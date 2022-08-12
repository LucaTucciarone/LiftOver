# LiftOver
## Liftover From Hg19 to Hg38
```
setwd(Directory)
bed.ls = dir(pattern = "Hg19.bed")
for (bed in bed.ls){
    bed.name = strsplit(bed, "Hg19.bed")[[1]][1]
    bed.name = paste(bed.name, "Hg38.bed", sep = "")
    message("liftOver ", bed, " /nfs/lab/publicdata/hg19ToHg38.over.chain.gz ", bed.name, " unMapped")
}
# Copy output to terminal and run
```

## Liftover From Hg38 to Hg19
```
setwd(Directory)
bed.ls = dir(pattern = "Hg38.bed")
for (bed in bed.ls){
    bed.name = strsplit(bed, "Hg38.bed")[[1]][1]
    bed.name = paste(bed.name, "Hg19.bed", sep = "")
    message("liftOver ", bed, " /nfs/lab/rlmelton/npod/notebooks/sherlock/Downstream_analysis_nPOD_april2022/ABC/Multiome_Islet/hg38ToHg19.over.chain ", bed.name, " unMapped")
}
# Copy output to terminal and run
```
