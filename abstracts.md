

## Abstracts

### Medical Genetics at Oslo University Hospital

*Hugues Fontenelle, Dept. of Medical Genetics, Oslo University Hospital, Norway*

At Scandinavia’s largest hospital we offer clinical diagnostics for rare hereditary diseases based on high-throughput sequencing.
Our bioinformatics pipelines mainly follows the GATK best practice guidelines for mapping and variant calling, plus custom
processing for quality control and report generation. We will talk about our experience with Nextflow in production and development,
including our setup in a secure cluster environment and how we currently use Docker in development, git-lfs for large files,
Python for glue and custom code.

[Slides](slides/hugues-fontenelle.pdf)

### Standardising Swedish genomics analyses using Nextflow

*Phil Ewels, Department of Biochemistry and Biophysics, Science for Life Laboratory, Stockholm, Sweden*

The SciLifeLab National Genomics Infrastructure is one of the largest sequencing facilities in Europe.
We are an accredited facility providing library preparation, sequencing, basic analysis and quality control for
Swedish research groups. Our sample throughput requires a highly automated and robust bioinformatics platform.
Until recently, we had multiple analysis pipelines built with a range of different workflow tools for each data type.
This made development work difficult and led to inevitable technical debt. In this talk I will describe how we
have migrated to Nextflow for a range of our data types, the difficulties that we faced and how we hope to leverage
Nextflow to migrate to the cloud in coming years.

[Slides](https://www.slideshare.net/tallphil/standardising-swedish-genomics-analyses-using-nextflow/1) 

### Building Pipelines to Support African Bioinformatics

*Scott Hazelhurst, University of the Witwatersrand, Johannesburg on behalf of the H3A Bionet Consortium, South Africa*

Bioinformatics is an example of a large-scale science application that requires complex pipelines for analysis.
The primary input data sets are very large and there are typically other secondary inputs (like reference genomes),
and analysis typically requires processing the data in several computationally-intensive phases with a number of different
program, the outputs of some being the inputs of others. Making such analyses reproducible, portable and easy for end-users
to run is a significant challenge, particularly in relatively resource-poor environments.
The Human Health and Heredity in Africa consortium (H3A) is a large African research consortium funded by the US National
Institutes of Health and the Wellcome Trust. H3A comprises over 20 collaborative centres and research projects conducting
genomics research, 3 biorepositories and the Pan-African Bioinformatics Network for H3Africa (H3ABioNet). One of the roles of
H3ABioNet is to build bioinformatics capacity to support H3A, and we have seen building pipelines to support key H3A workflows
as a priority.
As an initial project, H3ABioNet is building four pipelines for four key workflows and to gain experience.
The workflows covers (1) next generation sequence data; (2) metagenomics; (3) genome-wide association studies;
(4) imputation. The first two use CWL and the second two use Nextflow, and we see this a major activity of the
network over the next 5 years. This talk will give an overview of the pipelines, the process of building them
collaboratively and reflect on lessons learned, especially with respect to workflow languages.

[Slides](slides/Scott-Hazelhurst.pdf)

### Using Nextflow for Large Scale Benchmarking of Phylogenetic methods and tools

*Frédéric Lemoine, Institut Pasteur, Unité Bioinformatique Evolutive, Centre de Bioinformatique, Biostatistique et Biologie Intégrative, Paris, France*

Robustness of phylogenetic inferences is usually assessed by bootstrapping multiple sequence alignments.
However the use of the Felsenstein’s method, published in 1985, becomes questionable when analyzing big datasets.
In this context, we developed a new method to compute the bootstrap supports, which we benchmarked using large alignments of mammalian and HIV sequences. All workflows were implemented in Nextflow and executed on a large cluster environment, requiring thousands of CPU hours. The workflows produce different kind of results, such as trees, tabular files, R graphics, or tree images.

[Slides](slides/Frederic-Lemoine.pdf)

### Inside-Out: reproducible analysis of external data, inside containers with Nextflow

*Evan Floden, Comparative Bioinformatics, Centre for Genomic Regulation (CRG), Barcelona, Spain*

Container technology is revolutionising the data driven sciences. By providing the possibility to freeze
the software and the execution environment of experiments at run time, results can be made reproducible.
Whilst dependencies and operating systems can comfortably reside in version-controlled or hashed repositories
such as GitHub and Dockerhub, the vast quantities of both public and private genomic information are based in large
external databases. This provides a challenge to conducting reproducible analyses. I would like to use this talk to
open a discussion on the best approaches for use of databases with Nextflow. Using an example of the NCBI Sequence
Read Archive (SRA) and the accompanying NCBI-VDB API, I will demonstrate how open/secure and external/cached versions
of genomic databases can be accessed and analysed with Nextflow pipelines in a reproducible manner. Feedback from users
on their own use-case experiences and ideas into which ways Nextflow could help facilitate the ease-of-access of data
resources in the future will also be sought.

### Computational workflows for omics analyses at the International Agency for Research on Cancer

*Matthieu Foll, International Agency for Research on Cancer, Lyon, France*

In this presentation I will describe our use of nextflow to perform analyses of omics data at the International
Agency for Research on Cancer. I will explain why we needed such a tool and how we selected it over alternative ones.
I will discuss our choices of workflow design in the context of the multidisciplinary research performed in our Agency.
Finally, I will describe how nextflow has improved the overall quality of our research with a cost-benefit analysis and
report the problems or limitations we have identified.

[Slides](https://www.slideshare.net/MatthieuFoll/computational-workflows-for-omics-analyses-at-the-iarc)

### From zero to Nextflow @ CRG's Biocore

*Luca Cozzuto, Bioinformatics Core Facility, Centre for Genomic Regulation (CRG), Barcelona, Spain*

The Bioinformatics Core Facility implemented during the years a number of procedures and pipelines for providing
high quality results to an increasing number of users. Here we present our experience with migrating some of
extensively used pipelines to the Nextflow framework and creating docker/singularity containers for reproducibility.

[Slides](https://www.slideshare.net/lucacozzuto/from-zero-to-nextflow-2017)

### Standardizing life sciences datasets to improve studies reproducibility in the European Open Science Cloud

*Jordi Rambla, European Genome-Phenome Archive, CRG, Spain*

Services like the European Genome-phenome Archive ([EGA](https://ega-archive.org)) or big consortia portals
offer life science datasets for re-analysis at the requester computing facilities. This most of the times
results in redundant data analyses and resulting in significant waste of resources.
This presentation will give an overview how a proper data handling strategy, based on the FAIR principles,
can help to mitigate such problem, increasing the homology and interoperability between data for crossed analyses.
Moreover it will be discussed how to improve the efficiency and the reusability of such data analyses by
leveraging container technology and the Nextflow pipeline framework to deploy standard and reproducible
workflows in the European Open Science Cloud (EOSCD) infrastructure.

[Slides](slides/Jordi-Rambla.pdf)

### Nextflow for chemistry - crossing the divide

*Tim Dudgeon, Informatics Matters Ltd., UK*

Nextflow has become a useful workflow tool that is used in bioinformatics and genomics research.
We will describe some initial work we are doing that extends Nextflow's use into areas involving chemical
structures, and show how its scalability features can be of benefit to executing demanding computational
chemistry and cheminformatics workflows.
This work is part of the [OpenRiskNet](http://cordis.europa.eu/project/rcn/206759_en.html) project,
an EU Horizon 2020 funded project that CRG and Informatics Matters are participating.
This project is creating sustainable e-infrastructure to support chemical safety assessment,
such as prediction of chemical toxicology. Nextflow will be used for execution of computationally
demanding workflows that address these needs, as well as drug discovery tasks such as target and
ligand based virtual screening. We will describe examples of how chemistry functionality can be
used in Nextflow, and how this will be used in Informatics Matters web based workflow tool,
the [Squonk](http://squonk.it) Computational Notebook.

[Slides](slides/Tim-Dudgeon.pdf)

### Unbounded by Economics

*Angel Pizarro, AWS Research and Technical Computing, USA*

The cloud is as much an economic tool as it is a technological one. Violating some long held 
views about how computers are purchased (i.e. don’t buy one) can lead to a lot of weird ways in which
they can be used. And when we’re no longer bound by these old rules of engagement, we can solve some
difficult problems without noticing the effort. We’ll look at a few examples from various science domains,
and hopefully inspire you to think up some of your own.

### Simplifying shotgun metagenomic analysis with Nextflow

*Alessia Visconti, Department of Twins Research, King's College, UK*

Thanks to the increased cost-effectiveness of high-throughput technologies, the amount of data collected on microorganisms (bacteria, archaea, microbial eukaryotes, fungi, and viruses) has surged, boosting the development of software for their analysis. Nevertheless, researchers may not have the necessary expertise to define and implement data processing workflows nor to install and run software on their local machine or cluster.
By using the Nextflow framework, we developed a novel metagenomics analysis workflow, [YAMP](https://github.com/alesssia/YAMP), that is simple to use, easily portable, and very flexible and customisable. Moreover, the integration with a Docker container saves the users from the hassle of installing the required software, increasing, at the same time, the reproducibility of the results.

### Flexible bioinformatics workflows for NGS applications

*Johnny Wu and Amrita Pati, Roche Sequencing, Pleasanton, USA*

Targeted sequencing analyses supporting NGS assay development requires flexible and robust orchestration of analysis components in a portable manner. Using Nextflow, we have developed a bioinformatics workflow to support product development. Development of the workflow adhered to the design control process for medical devices as guided by the US FDA. Nextflow, paired with the Docker containerization technology, was chosen to execute the bioinformatics workflow on multiple compute infrastructures across sites within the organization. Characterization of the workflow ensures that turnaround time and performance requirements are achieved. We present the bioinformatics workflow and its utilization in our product development ecosystem.

### Putting the Computation in Computational Biology

*Mike Smoot, Synthetic Genomics, La Jolla, CA, USA*

Synthetic Genomics uses Nextflow for many of its bioinformatics pipelines. This talk describes the cloud infrastructure that we have designed to accommodate the variable demands of our pipelines and users. I will discuss the elements of our software stack, the basic architecture of our cloud configuration, and our cluster design.  Topics will include how our infrastructure scales to meet increased demand, design elements of our pipelines to facilitate cloud execution, integration with external services, and other aspects of our system that may be of interest to the Nextflow community.
