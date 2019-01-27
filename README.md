# FAIR Embeddings for Textual Cultural Heritage #

Valid and scalable solutions to research questions for textual cultural heritage (TeCH) data will increasingly depend on access to so-called neural embeddings. Neural embeddings are abstract and distributed dense representations of language (characters, words, phrases) that are learned by data-intensive representation-learning algorithms implemented as deep neural network architecture. To ensure that DH researchers uses state-of-the-art technology for tackling complex TeCH problems, it is mandatory that they have access to pre-trained multi-level embeddings for their respective language, which follow the FAIR principles (findable, accessible, interoperable, and resuable). FAIR Embeddings for Textual Cultural Heritage (FAIR eTeCH) will pioneer FAIR embeddings for Scandinavian languages, which through a collaboration with national libraries and an innovative use of regulations pertaining to derived data can circumvent restriction on copyrighted and sensitive data.

One of the greatest challenges for large scale DH research is access to original or direct data (e.g., the content of newspaper article) because of copyright restrictions. In Denmark, for instance, a newspaper article in the *Danish Mediastream* has to be more than a century old in order to allow a researcher free data mining access. Embeddings however have status as derived data that do not allow for a reconstruction of the original data source. Embeddings trained on large newspaper collections are more than adequate to solve problems related to semantic similarity and drift.

---
**Publication date:**

**DOI:**

**License (for files)**

---


---
**Versions**


**Cite all version?**
---

---
**Share**

**Cite as**
---

---
**Export**
---

## Example of Use ##

### Download pre-trained embeddings ###

```bash

git clone https://github.com/knielbo/fair-etech.git
cd fair-etech
 

```


### Load text models in Python ###

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
