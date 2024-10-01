## **HW1**
### **“Where Do We Come From? What Are We? Where Are We Going?”**

> Phylogenetics, human evolution.

This work was devoted to reconstructing an evolutionary tree based on human mtDNA data as well as estimating the age of mitochondrial Eve and the most recent common ancestor of modern humans and Neanderthals.

Mitochondrial Eve is the woman from whom all modern humans inherit mitochondrial DNA, which is passed on exclusively through the maternal line. She is said to have lived about 200,000 years ago in East Africa and is a key figure supporting the theory that all humans share a common African ancestry. 

---
**Steps:**

1.   Alignment using MAFFT (or MUSCLE, CLUSTAL W, prank etc)
2.   Tree reconstruction using IQTree (or FastTree, MEGA etc)
3.   Root the tree (add Neanderthal and Denisovan samples as outgroup)
4.   Tree visualization using ETE Toolkit and ITOL (or MEGA, Python, R etc)
5.   Add myself to tree to see what group do I belong to

Data:
* Human mtDNA data *([click here for data](https://figshare.com/ndownloader/files/30768763))*

For outgroup:
* Neanderthal samples *([click here for data](https://figshare.com/ndownloader/files/30768766))*

* Denisovan samples *([click here for data](https://figshare.com/ndownloader/files/30768775))*

---

### **1. Tree reconstruction**

We can look at the tree before and after rooting using Neanderthal and Denisovan samples.

<img width="690" alt="Снимок экрана 2024-09-26 в 23 32 00" src="https://github.com/user-attachments/assets/10c457c5-49c0-4686-90a0-da3417003188">

Despite the fact that at first glance it may seem that the tree does not correspond to reality because of the names that include the names of countries, if you pay attention to the haplogroups, they are well grouped together.

---

### **2. Age revealing**

After building and rooting the tree, the approximate age of mitochondrial Eve was determined, which was calculated using the number of mutations, which is only a rough estimate because it does not take into account many factors. Nevertheless, the obtained age agrees with data from different sources that estimate the age of mitochondrial Eve in the range from 100 to 200 thousand years. The age that was obtained with our calculations was approximately 180 thousand years.

**Estimated age of mitochondrial Eve according to the maximum: 192000 years**

**Estimated age of mitochondrial Eve by average: 170227 years**

The same method was used to determine the age of the most recent common ancestor of modern humans and Neanderthal. It amounted to approximately 436000 years, which also agrees with data from various sources (at least the orders of magnitude coincide).

---

### **3. Adding myself**

In addition, my mitochondrial dna data were added to the final tree to see which haplogroup I belong to. this image shows that I belong to haplogroup H, which given the description of this group may well be true. 


<img width="615" alt="Снимок экрана 2024-09-25 в 23 11 05" src="https://github.com/user-attachments/assets/cdc3e0e6-f8fb-4d4f-b322-3ba68c30cea2">


"...haplogroup H is the most common maternal lineage in Europe, with more than half of the modern female population of Northwestern Europe belonging to it. The frequency of haplogroup H in Europe ranges from 40% to 50%. It is also frequent in North Africa and the Middle East, but its distribution decreases toward the southeast.
The mutation that defines haplogroup H occurred about 25,000 to 30,000 years ago in southwest Asia or the Middle East. To date, about 90 major lineages or subclades of haplogroup H have been identified, most of which are subdivided into smaller subclades."

> However, only using our data it is difficult to say more precisely to which subclade I belong. 

---

### **3.2 Mistakes correction**

** There were some mistakes found in the last part of work that was about adding my mtDNA to the tree.

**The corrected version looks like this**

<img width="524" alt="Снимок экрана 2024-10-01 в 16 47 15" src="https://github.com/user-attachments/assets/1fa1cd64-8ffd-4502-9ca5-aae5a9567dfe">

The haplogroup C (C4 according to Genotek) and just interesting image of haplogroup tree below.

<img width="922" alt="Снимок экрана 2024-10-01 в 15 57 40" src="https://github.com/user-attachments/assets/e8b6fda6-0c74-4243-86c5-017e41913191">

The mistake appeared cause I've used the wrong reference and that's the code to get the right one.
```
!wget https://hgdownload.soe.ucsc.edu/goldenPath/hg19/bigZips/hg19.fa.gz
!zcat /content/hg19.fa.gz | awk '/^>chrM/{flag=1;print;next} /^>/{flag=0} flag' > /content/ucsc_MT_hg19.fasta   
```
