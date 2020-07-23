# OS 1 Course Project  

###Time period: FOUR weeks

**Goal**: Build a further understanding of Operating Systems, especially the file system part.

This year, we want you to build an understanding of parallel file system, especailly high performance file systems, and play with a open-sources file system - PLFS (parallel log-structured file system). There are majorly few steps towards your course project:

*Step 1*: You need to download the recommanded version from <https://github.com/plfs/plfs-core>, and install the file system on your own Linux machine (a laptop, a desktop, or even a server). In this step, you need to follow the **README**. You should carefully read the **README.install** file, otherwise you may not be able to install PLFS.  You should read the all the README documents if necessary  

*Step 2*: After the step1, your PLFS should work properly. I can imagine that you may not have any clue of the PLFS, even thought it "works". In this step, you are required to read the technique paper called **PLFS: A Checkpoint Filesystem for Parallel Applications**. I am counting on you to read at least the following parts of the conceptual document: **Introduction**, **Design of An Interposition Layer**, and **Evaluation: MPI-IO Test**. If you are interested in the background of high performance file systems, you can read **Background** section, but it is not required in this step.

*Step 3*: Now you are surpposed to have some general ideas of PLFS. In this step, you are about to write a reading report for the technical paper **PLFS: A Checkpoint Filesystem for Parallel Applications**. I believe you've already have experiences in writing a reading report. Here are some advises for you on how to read a technical paper. It will be helpful if you have a time budget for the 12-page paper. <https://www.cs.jhu.edu/~jason/advice/how-to-read-a-paper.html> and <https://web.stanford.edu/class/ee384m/Handouts/HowtoReadPaper.pdf>

*Step 4:* Writing a reading report may not be very time consumption, but you may be confused by the idea of PLFS. Let's read PLFS's source code. In this step, you need to read the PLFS's source code and draw its flow diagram. To be more sepecific, you should draw flow diagrams of four fundamental I/O operations: *open, read, write,* and *close*. I suggest you to use GDB to trace all the related functions and pay attention to the passed parameters.  

*Step 5:* In this step, let's test the I/O performance of your PLFS using MPI-IO Test benchmark <http://freshmeat.sourceforge.net/projects/mpiiotest>. MPI-IO Test is a LANL synthetic checkpoint I/O benchmark tool. You only need to test PLFS N-1 write pattern with three "Number of Processes" setups: 1, 2, and 4. For those who are willing to explore, you may install a parallel file system such as PVFS or Lustre to see how PLFS improve multi-process write performacne. You can come to me to have further tests on the  parallel file system in my lab. But you have to finish all the required parts for the course project.

**Source data**: 

1. PLFS https://github.com/plfs/plfs-core>
2. General Guide <https://github.com/plfs/plfs-core/blob/master/README>
3. Installation Guide <https://github.com/plfs/plfs-core/blob/master/README.install>
4. MPI-IO Test Benchmark http://freshmeat.sourceforge.net/projects/mpiiotest
5. PLFS Technique Paper <https://www.pdl.cmu.edu/PDL-FTP/PDSI/plfs.pdf>

**Present Results**: You are supposed to present the following materials in your final report:

- **Part 1**: Project Report 
  - A reading report of the PLFS paper. Please  **DO NOT** copy and paste from the original paper. Try to rephrase it using your own language. The report should be at least two pages. 
  - MPI-IO Experimental results and brief results evluation or intepretation.
  - A summary of lesson learned from the entire course project. Anything or ideas can be shared here.
- **Part 2**: PLFS Source Code Flow Diagram
  - The Flow Diagram requires four seperated flow chart of four fundamental PLFS I/O operations accordingly (i.e., *open, read, write*, and *close*). 

**Report Format**: Please be noted that the report (including the project report and the literature review ) is using **IEEEconf** template (10pt, double column). The Latex version can be downloaded from the website. (https://www.ieee.org/content/dam/ieee-org/ieee/web/org/conferences/Conference-LaTeX-template_7-9-18.zip)

**Diagram Format:** There is no specific requirement on the diagram layout, as long as you are using a professional diagram drawing tools such as Visio, OmniGraffle, or you can try Markdown to do so. Please be noted that the diagram should be **in .eps file format**.

**Hints**: 

1. You may need to contact TAs and raise a question on Piazza during the PLFS install and MPI-IO Test configuration.
2. There will be some flags correctly set before you can run PLFS in a debug mode.
3. While you are reading the source code, you should keep the Fig 4 in mind. The figure will help you to better understand what PLFS is doing. 
4. If you have troubles on your test results presentation, you can refer to the PLFS paper Fig. 5(a) to see how they handle it. 
