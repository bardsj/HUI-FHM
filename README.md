# High Utility Itemset Mining

Implementation of the FHM high utility frequent itemset mining algorithm:

Fournier-Viger, P., Wu, C.-W., Zida, S., Tseng, V. S.: FHM: Faster high-utility
itemset mining using estimated utility co-occurrence pruning. In: Proc. 21st Intern.
Symp. on Methodologies for Intell. Syst., pp. 83{92 (2014)  

Uses only the Python standard library.
   
---

## Usage

```
>>> from HighUtilityItemsetMining import FHM
>>> transactions = [
...     (1,[('a',3),('b',2)]),
...     (2,[('a',1)]),
...     (3,[('c',1),('b',10)]),
...     (4,[('a',7),('b',1),('c',2)])
... ]
>>> external_utilities = {
...     'a': 4,
...     'b': 2,
...     'c': 7
... }
>>> fhm = FHM(transactions,external_utilities,0.3,minutil_pc=False)
>>> fhm.run_FHM()
[(['a'], 44), (['a', 'c'], 42), (['a', 'b'], 46), (['c'], 21), (['c', 'b'], 43), (['b'], 26)]

```