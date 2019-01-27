
<p align="center">
  <b>xxxxx This is a mockup site, data and links are empty xxxxx</b><br>
  <br><br>
</p>

# FAIR Embeddings for Textual Cultural Heritage #

Valid and scalable solutions to research questions for textual cultural heritage (TeCH) data depend on access to contextualized embeddings. Word embeddings are abstract and distributed dense representations of language (characters, words, phrases) that are learned by data-intensive representation-learning algorithms implemented as deep neural network architecture. To ensure that DH researchers uses state-of-the-art technology for tackling complex TeCH problems, it is mandatory that they have access to pre-trained multi-level embeddings for their respective language, which follow the FAIR principles (findable, accessible, interoperable, and resuable). FAIR Embeddings for Textual Cultural Heritage (FAIR eTeCH) will pioneer FAIR embeddings for Scandinavian languages, which through a collaboration with national libraries and an innovative use of regulations pertaining to derived data can circumvent restriction on copyrighted and sensitive data.

One of the greatest challenges for large scale DH research is access to original or direct data (e.g., the content of newspaper article) because of copyright restrictions. In Denmark, for instance, a newspaper article in the *Danish Mediastream* has to be more than a century old in order to allow a researcher free data mining access. Embeddings however have status as derived data that do not allow for a reconstruction of the original data source. Embeddings trained on large newspaper collections are more than adequate to solve problems related to semantic similarity and drift.

---
**Publication date:**

January 28, 2019

**DOI:**

[DOI: 00.0000/zenodo.0000002](https://doi.org/00.0000/zenodo.0000002)

**License (for files)**
[Creative Commons Attribution 4.0 International](http://creativecommons.org/licenses/by/4.0/legalcode)

---

---
**Versions**

|Version|Date|
|---|---|
|Version 1 00.0000/zenodo.0000001|Jan 28, 2019|
|Version 2 00.0000/zenodo.0000002|May 23, 2019|

**Cite all versions?**
You can cite all versions by using the DOI 00.0000/zenodo.0000000. This DOI represents all versions, and will always resolve to the latest one. [Read more](http://help.zenodo.org/#versioning).

---

---
**Share**

[LINKS HERE for export to SOME]

**Cite as**


@misc{nielbo_2019_0000002,  
  author    = {Nielbo,Gerdes and Møldrup-Dalum},  
  title     = {{FAIR Embeddings for Textual Cultural Heritage}},  
  month     = dec,  
  year      = 2019,  
  doi       = {00.0000/zenodo.0000002},  
  url       = {https://doi.org/00.0000/zenodo.0000002}  
}

---


---
**Export**

[BibTex](https://zenodo.org/record/0000002/export/hx),
[DataCite](https://zenodo.org/record/0000002/dcite4),
[JSON](https://zenodo.org/record/0000002/export/json),
[Mendeley](https://www.mendeley.com/import/?url=https://zenodo.org/record/0000002)

---

## Example of Use ##

**Download pre-trained embeddings**

```bash

git clone https://github.com/knielbo/fair-etech.git
unzip fair-etech.zip
cd fair-etech

```


**Load text models in Python**

```py

import io

def load_vectors(filename):
    f = io.open(filename, 'r', encoding='utf-8', newline='\n', errors='ignore')
    n, d = map(int, f.readline().split())
    data = {}
    for line in f:
        tokens = line.rstrip().split(' ')
        data[tokens[0]] = map(float, tokens[1:])
    return data
```
