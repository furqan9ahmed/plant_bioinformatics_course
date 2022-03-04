# **Plant Bioinformatics Method-I** 
[Here is the link of this course](https://www.coursera.org/learn/bioinformatics-methods-1/lecture/gnPjk/lecture)

I started learning this course on 02.03.2022 after the presentation of progress report in IFAM, Uni Kiel, Germany.

> ## **What is bioinformatics?**
Bioinformatics:
- is the development of application of computational tools in manging all kinds of biological data
- involves the technology that uses computers for storage, retrieval, manipulation, and distribution of information related to biological macromolecules such as DNA, RNA, proteins, and metabolites
- generally limted to sequence, structural, and functional analysis of genes and genomes, and their corresponding products
- sometimes called computational molecular biology
---
This field has really developed in the past 15 years due to the efforts of genome sequencing projects, such as the [human genome sequencing project](https://www.genome.gov/human-genome-project).

> ## **Why do we need bioinformatics?**

- How do we deal with three billion pieces of sequence information? 
- So why do we need bioinformatics? 
- Well, if you can imagine three billion letters in the human genome, three billion nucleotides, how do you really make sense of that without using computers? 

> ## Biological databases
> The other thing that bioinformatics is about is biological databases, how we can store these biological data
1. **Why databases are used?**

To archive accumulated knowledge and to provide scientists with easy access to biological data.

2. **What is a database? What are the Data structures: Flat file databses vs Rational databases?**

How can we store the files in databases? 
- **Flat File Format:**

One type is Flat File format with fields separated by some delimiters. Here is an example.

![img1](resources/flat_file.png) 

There is a problem with flat file format database, as there are some retundencies in the file. Same information is repeated many times.

- **Relational Databases**

Relational databases consists of relations (tables) containing attributes (columns or fileds).\
Each row in a table is known as tupple or records similar to pythons. 
> _If you are interested in learning Data Science with Python ( a 40 days course) in urdu/Hindi language you can browse follwoing playlist ([Python ka Chilla with Baba Aammar](https://www.youtube.com/watch?v=QvPekMN4F0w&list=PL9XvIvvVL50HVsu-Ao8NBr0UJSO8O6lBI)_)

Here is another detailed example from Plant Bioinformatics Course on Coursera
![img2](resources/flat_file2.png)

Foriegn key is used to link tables with similar information of one or more columns. Which is actually the primary key of a column of contacts in the second table.

SQL (Structured Querry Language) is an example of querry database and we will cover this in a separate crash course in urdu/hindi language, link is coming soon.

> **Accession numbers and identifiers (genebank flat file format)**\
> Many of the biological databases (Genebank, UNIPROT etc.) have several ways to identify a specific given entry:
> - Identifier
> - Accession code (or a specific number)

Here is the detailed version of that:
![img3](resources/img3.png)

Another popular type is the accession number or accession code:
> **Accession number or accession code:**\
> An accession code (or number) is a number (with a few characters in front) that uniquely identifies an entry.\
> It is often assigned arbitrarily. For example, the
accession code for ADH6_HUMAN in UNIPROT is P28332.In the case of GenBank, the accession code for the human ADH6 gene
sequence is AH001409.

**Versioning of sequences GenBank**:\
Records typically contain the Accession.Version identifier, such as **AHO01409.2**, in the VERSION Iine of the record. This identifier used to be mapped to its corresponding GI* number, which was like the "primary key" of GenBank.

>- To specify a sequence exactly in GenBank, use its _**Accession.Version**_.
> - To retrieve the most up-to-date sequence, use the accession number without
version: the most up-to-date sequence will be retrieved automatically. 

The GI (Genlnfo ldentifier) system was deprecated as of 2016 use Accession.Version only to
retrieve a specific sequence - but you will still see Gls in GenBank records!

> **A pratical example of utility - NCBI Search (GQuery/Entrez)**\
> Human alcohol dehydrogenase VI gene to find with the following [link](https://www.ncbi.nlm.nih.gov/nuccore/AH001409)

**After going to the link following information will appear:**
![img4](resources/img4.png)
![img5](resources/img5.png)
![img6](resources/img6.png)
![img7](resources/img7.png)

> _**Note: in some records we may see a CDS (Coding sequence) feature followed by the sequence itself as following:**_


![img8](resources/img8.png)
![img9](resources/img9.png)

---
<span style="color:#1ba69a">**From 1982 to February 2020, GenBank statistics can be found on the [this link](https://www.ncbi.nlm.nih.gov/genbank/statistics/)**</span>

Currently it is showing something like this:
![img10](resources/img10.png)

<span style="color:#1ba69a">### **How to Search Sequences:**</span>

Searching GenBank or other sequencing databases (DBs) can be done using:
1. keywords
2. using sequence similarity using [NCBI BLAST](https://blast.ncbi.nlm.nih.gov/Blast.cgi)

<span style="color:Red">**Google and other search engines can not search sequence similarities better than blasting, because tehse search engines can not run partial matches to similar sequence with gaps and they also don't which amino acids have similar properties.**</span>

Here's you can use [blast in NCBI](https://blast.ncbi.nlm.nih.gov/Blast.cgi?PROGRAM=blastn&PAGE_TYPE=BlastSearch&LINK_LOC=blasthome)
![img11](resources/img11.png)

<!-- 
#this is how you can add colors to text but it will not work in .md files on github doc

<span style="color:blue">Your text here</span>

 -->

<span style="color:blue">**Important Terms and Definitions:**</span>

Please google these and clear your concepts
1. Homologs
2. Paralogs
3. Orthologs
4. Speciation
5. Gene duplication
6. SNPs

### **Searching across DBs: the NCBI Search tool**

[NCBI Seach tool](https://www.ncbi.nlm.nih.gov/search/) (previously known as ENtrez/GQuery) is one of the best tools to search DBs. NCBI Search provides links between many of the DBs at NCBI. 

**Example:**

Identify the SNPs which potentially cause early onset breast cancer, and design oligos to PCR them in samples of human genomic DNA for sequencing.\
We can use OMIM (Online Mendelian Inheritance in Man) database from the list of the DBs on the left side of search bar.\
OMIM has links to everything that is known about a given disease across the various DBs at NCBI.

![img12](resources/img12.png)
Click on **"Gene Summaries"**

![img13](resources/img13.png)

We can find SNPs use a tool called primer3 to design a primer of that specific SNP, to find out the variation in the person genomic DNA sample.
This process will take less than 15 minutes to find a solution and methodology to a problem.\
This one set of information will help us to find the incredible set of information stored in NCBI.

In the upcoming lecture, we will be talking about blast.

We can also use [NCBI's variation viewer](https://www.ncbi.nlm.nih.gov/variation/view) to find non-synonymous SNPs information. 

![img14](resources/img14.png)


---

# **Pre-requisists to search on NCBI:**

The National Center for Biotechnology Information (NCBI)maintained by the US National Library of Medicine and National Institutes of Health is one of the world’s most important resources and repositories for biological data.

Entire genomes, from viruses to humans, are compiled, organized, and cross-referenced within these networks, such that surfing the genome can be almost as easy as surfing the web.

But you must know the following before starting your search on NCBI: 
1. What you are looking _**for**_?
2. What you are looking _**at**_?

to get out of these DBs.\
**We will learn these in the following section**

Normally google and other search engines do not index database driven websites, which is why it can not be used for searching the information stored in databases such as NCBI.

Google can not handle protein searching as well as it can not handle sequence searching.

We will go step by step to explore [NCBI website](https://www.ncbi.nlm.nih.gov/) which is constantly being updated.

We can read the about NCBi and Search via _**search tool of NCBI**_ (formerly known as GQuery or Entrez) in the search bar to go to the specific topic as shown here:

![img15](resources/img15.png)

When you go to the searchbar and type **_Bacteria_** it will give you a whole list of hits in each section. This search will give us millions of hits which is not specific for research purposes. We should narrow it down.
Here's what it looks like:

![img16](resources/img16.png)

### **Example:**

Usually when searching these databases, you have either a region of DNA or a protein (or protein function) of interest. For this lab you’ll be using a gene from **_Arabidopsis thaliana_**, a small flowering plant that is like the fruit fly of the plant world as it has a comparatively rapid life cycle and requires little space to grow. The protein product of this gene is recorded under _**accession number NP_001318308**_, and it is an E3 ligase, involved in ubiquitination of proteins, which is a signal for their degradation.