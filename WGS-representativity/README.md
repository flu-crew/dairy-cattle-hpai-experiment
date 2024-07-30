### WGS representativity analysis of  A/dairy_cattle/Texas/24-008749-002/2024 ###

1. We downloaded SRA assemblies of cattle H5N1 genes from [BV-BRC](https://www.bv-brc.org/view/Taxonomy/11320#view_tab=genomes&filter=and(eq(subtype,%22H5N1%22),eq(collection_year,%222024%22),eq(geographic_group,%22North%20America%22),ne(genbank_accessions,*))&defaultColumns=-cds,h5_clade,segment,sra_accession,collection_date,-genbank_accessions&defaultSort=genome_name,segment) on June 13, 2024. These strains were merged with the previously published B3.13 strains and the duplicates were removed. This resulted in n=367 whole genome B3.13 sequences, 334 of which were from cattle.

2. We built a WGS phylogeny from the concatenated whole genome sequences using IQ-Tree 2 as follows
```
iqtree2 -s combined.aln -spp iqtree.partitions.nexus -B 1000 -bnni -redo
mv iqtree.partitions.nexus.treefile cattle.all.wgs.tre
```

3. We built a consensus WGS of cattle strains using [smof](https://github.com/incertae-sedis/smof).
```
cat combined.aln | smof grep "cattle" | smof consensus > cattle.consensus.fasta
```
And compared the `A/dairy_cattle/Texas/24-008749-002/2024` genome with the consensus genome in UGENE.

4. We evaluated the representativity of `A/dairy_cattle/Texas/24-008749-002/2024` using [PARNAS](https://github.com/flu-crew/parnas).
```
parnas -t cattle.all.wgs.tre --prior ".*Texas/24-008749-002/2024.*" --evaluate --constrain-fully ".*cattle.*"
```
