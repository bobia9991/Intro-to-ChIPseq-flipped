# Workshop Schedule

> **NOTE:** The *Basic Data Skills* [Introduction to the command-line interface](https://hbctraining.github.io/Intro-to-shell-flipped/schedule/) workshop is a prerequisite.


## Pre-reading:

* Please **study the contents** and **work through all the exercises** within the following lessons:
  * [Shell basics review](https://hbctraining.github.io/Intro-to-rnaseq-hpc-salmon-flipped/lessons/shell_review.html)
  * [Best Practices in Research Data Management (RDM)](https://hbctraining.github.io/Intro-to-rnaseq-hpc-salmon-flipped/lessons/04a_data_organization.html)
  
  
## Day 1

| Time |  Topic  | Instructor |
|:-----------:|:----------:|:--------:|
| 1:30 - 1:45 | [Workshop Introduction](https://github.com/hbctraining/Intro-to-ChIPseq-flipped/blob/main/lectures/Intro_to_workshop.pdf) | Meeta |
| 1:45 - 3:00 | [Introduction to ChIP-seq](https://www.dropbox.com/s/k2xgo8sk8werzxa/Introduction%20to%20ChIP-seq%202022.pdf?dl=1) | Meeta |
| 3:00 - 3:05 | Break|  |
| 3:05 - 3:50 | [Working in an HPC environment](https://hbctraining.github.io/Intro-to-rnaseq-hpc-salmon-flipped/lessons/03_working_on_HPC.html) | Jihe 
| 3:50 - 4:00 | Overview of self-learning materials and homework submission | Jihe |


### Before the next class:

I. Please **study the contents** and **work through all the code** within the following lessons:
   1. [Experimental design considerations and understanding the ChIP-seq workflow](../lessons/01_ChIPseq_design_and_workflow.md)
      <details>
       <summary><i>Click here for a preview of this lesson</i></summary>
         <br>Before you begin thinking about performing a ChIP-seq experiment, it is important to plan for it. There are many things to consider depending on the cells you are working with, and your protein of interest. <br><br>In this lesson, we will:<br>
             - Review different types of controls for ChIP-seq<br>
             - Highlight the sequencing considerations for different binding profiles<br>
             - Introduce you to the ChIP-seq analysis workflow<br><br>
        </details>
   
   2. [Dataset overview and project organization](../lessons/02_dataset_and_project_setup.md)
      <details>
       <summary><i>Click here for a preview of this lesson</i></summary>
         <br>We are ready (and excited!) to get started with our ChIP-seq analysis. But, wait! There are just a few things to do before we get our hands on the data. <br><br>In this lesson you will:<br>
            - Learn about the dataset we are using in this workshop<br>
            - Organize your space, so you are setup for success<br><br>
         </details>

   3. [Quality Control of Sequence Data: Running FASTQC and evaluating results](../lessons/03_QC_FASTQC.md)
      <details>
       <summary><i>Click here for a preview of this lesson</i></summary>
         <br>The first step of most NGS analyses is to evaluate the quality of your sequencing reads. <br><br>In this lesson you will explore:<br>
            - The FASTQC software, and how to run it on your raw sequencing data<br>
            - The HTML report that is returned from FASTQC and how to interepret the different plots<br><br>
        </details>
        
   4. [Alignment using Bowtie2](../lessons/04_alignment_using_bowtie2.md)
      <details>
       <summary><i>Click here for a preview of this lesson</i></summary>
         <br>The next step is taking our high quality reads and figuring out where in the genome the originated from. In theory this seems like a simple task, but in practice it is quite challenging. <br><br>In this lesson you will cover:<br>
            - The Bowtie2 software, a popular tool for aligning DNA sequence reads<br>
            - Alignment file formats<br>
            - How to run your alignment as a job on the cluster<br><br>
        </details>


> **NOTE:** To run through the code above, you will need to be **logged into O2** and **working on a compute node** (i.e. your command prompt should have the word `compute` in it).
> 1. Log in using `ssh rc_trainingXX@o2.hms.harvard.edu` and enter your password (replace the "XX" in the username with the number you were assigned in class). 
> 2. Once you are on the login node, use `srun --pty -p interactive -t 0-2:30 --mem 1G /bin/bash` to get on a compute node or as specified in the lesson. > 3. Proceed only once your command prompt has the word `compute` in it.
> 4. If you log out between lessons (using the `exit` command twice), please follow points 1. and 2. above to log back in and get on a compute node when you restart with the self learning.
>

2. **Complete the exercises**:
   * Each lesson above contain exercises; please go through each of them.
   * **Copy over** your code from the exercises into a text file. 
   * **Upload the saved text file** to [Dropbox](https://www.dropbox.com/request/9kCUWtXRx1P2AZNsR8qQ) the **day before the next class**.

### Questions?
* ***If you get stuck due to an error*** while runnning code in the lesson, [email us](mailto:hbctraining@hsph.harvard.edu) 
* Post any **conceptual questions** that you would like to have **reviewed in class** [here](https://PollEv.com/hbctraining945).

## Day 2

| Time |  Topic  | Instructor |
|:-----------:|:----------:|:--------:|
| 1:30 - 2:15 | Self-learning lessons review |  All |
| 2:15 - 3:00 | [Filtering BAM files](../lessons/05_filtering_BAM_files.md) | Jihe |
| 3:00 - 3:05 | Break|  |
| 3:05 - 4:00 | [Peak calling](../lessons/06_peak_calling_macs.md) | Meeta |

### Before the next class:

I. Please **study the contents** and **work through all the code** within the following lessons:
   1. [Handling peak files using `bedtools`](../lessons/07_handling_peaks_bedtools.md)
      <details>
       <summary><i>Click here for a preview of this lesson</i></summary>
         <br>Now that we have called peaks for each of our samples, it's time to look at the output. The output of MACS2 includes various files, with the narrowPeak file being the most important for interpretation. <br><br>In this lesson you will cover:<br>
             - The basics of the BED file format (and how it extends to narrowPeak files)<br>
             - The bedtools suite of tools<br>
             - Filtering and intersecting BED files <br><br>
        </details>
   
   2. [Creating bigWig files](../lessons/08_creating_bigwig_files.md)
      <details>
       <summary><i>Click here for a preview of this lesson</i></summary>
         <br>ChIP-seq data is best evaluated by visualizing peaks. However, in order to do so we require the appropriate file formats.
         <br><br>In this lesson you will:<br>
            - Learn about different file formats for peak visualization<br>
            - Create bigWig files<br><br>
         </details>

   3. [Qualitative assessment of peak enrichment using deepTools](../lessons/09_data_visualization.md)
      <details>
       <summary><i>Click here for a preview of this lesson</i></summary>
         <br>An exciting component of ChIP-seq analysis is to be able to visualize your results, and gain some biologically meaningful insight. This may in turn generate hypothesis for you to further explore with your data!  <br><br>In this lesson you will learn:<br>
            - How to use deepTools to create heatmaps and profile plots<br>
            - To ask questions about your data and find answers through visualization<br><br>
        </details>



2. **Complete the exercises**:
   * Each lesson above contain exercises; please go through each of them.
   * **Copy over** your code from the exercises into a text file. 
   * **Upload the saved text file** to [Dropbox](https://www.dropbox.com/request/KYkDi8pcJue9wlrPnNOu) the **day before the next class**.
   
### Questions?
* ***If you get stuck due to an error*** while runnning code in the lesson, [email us](mailto:hbctraining@hsph.harvard.edu) 
* Post any **conceptual questions** that you would like to have **reviewed in class** [here](https://PollEv.com/hbctraining945).

***

## Day 3

| Time |  Topic  | Instructor |
|:-----------:|:----------:|:--------:|
| 1:30 - 2:00 | Self-learning lessons review | All |
| 2:00 - 2:30 | [Troubleshooting your ChIP-seq analysis](../lessons/troubleshooting_chipseq_partI.md) | Meeta |
| 2:30 - 2:35 | Break|  |
| 2:35 - 3:45 | [Automating the ChIP-seq workflow](../lessons/10_automation_new.md) | Jihe |
| 3:45 - 4:00 | [Wrap-up](../lectures/Wrap-up_new.pdf) | Meeta |


## Answer keys

* Day 1 exercises 
  * [Data Management and project organization](../homework/Day1_readme_answerkey.md)
  * [QC and Alignment questions](../homework/Day1_answer_key.md)

* Day 2 exercises 
  * [Handling peak calls](../homework/Day2_answer_key.md)

* Day 3 In-class 
  * [Automation shell script](../homework/chipseq_analysis_on_input_file.sh)
  * [Parallelization script](../homework/chipseq_run_allfiles.sh)

***

## Resources
* ENCODE Data Standards and Processing Pipeline Information for [Histone](https://www.encodeproject.org/chip-seq/histone/) and [Transcription Factors](https://www.encodeproject.org/chip-seq/transcription_factor/)
* [ENCODE guidelines and practices for ChIP-seq](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3431496/). An older paper, but a good outline of general best practices.
* Experimental design considerations:
    * [Thermofisher Step-by-step guide to a successful ChIP experiment](https://www.thermofisher.com/us/en/home/life-science/antibodies/antibodies-learning-center/antibodies-resource-library/antibody-application-notes/step-by-step-guide-successful-chip-assays.html)
    * "Chromatin Immunoprecipitation (ChIP) Principles and How to Obtain Quality Results", [BenchSci Blog](https://blog.benchsci.com/chromatin-immunoprecipitation-chip-principles-and-how-to-obtain-quality-results)
    * [O’Geen et al (2011), Methods Mol Biol](https://pubmed.ncbi.nlm.nih.gov/21913086/) - A focus on performing ChIP assays to characterize histone modifications
* [Jung et al (2014). NAR.](https://academic.oup.com/nar/article/42/9/e74/1248114) - Impact of sequencing depth in ChIP-seq experiments 



## Building on this workshop
* [Integration of ChIP-seq and RNA-seq](../lessons/integrating_rna-seq_and_chip-seq.md)
* [A Brief Introduction to CUT&RUN](../CUT&RUN/Intro_to_CUT&RUN.md)
* [Advanced bash commands (aliases, copying files, and symlinks)](https://hbctraining.github.io/Intro-to-rnaseq-hpc-salmon-flipped/lessons/more_bash_cluster.html)
* [Introduction to R workshop materials](https://hbctraining.github.io/Intro-to-R-flipped/#lessons) 


***

*These materials have been developed by members of the teaching team at the [Harvard Chan Bioinformatics Core (HBC)](http://bioinformatics.sph.harvard.edu/). These are open access materials distributed under the terms of the [Creative Commons Attribution license](https://creativecommons.org/licenses/by/4.0/) (CC BY 4.0), which permits unrestricted use, distribution, and reproduction in any medium, provided the original author and source are credited.*
