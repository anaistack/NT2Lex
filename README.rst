NT2Lex
======

.. image:: https://img.shields.io/badge/version-0.0.0-blue
   :target: https://github.com/anaistack/NT2Lex/tree/main
   :alt: package version

`NT2Lex <https://cental.uclouvain.be/nt2lex/>`_ is a lexical database for Dutch as a foreign language (NT2). The resource includes frequency distributions of words observed in texts graded along the Common European Framework of Reference for Languages (CEFR) scale. It is a receptive lexicon as it includes word frequencies observed in textbook reading activities and simplified readers targeting learners of Dutch. 

The resource comes in two versions: a basic version (CGN) and an extended version (CGN+ODWN). 

NT2Lex-CGN
   The basic version includes 15,227 lexical entries that have been lemmatized and part-of-speech tagged with `Frog Tagger <https://languagemachines.github.io/frog/>`__. A simplified version of the `CGN tagset <http://nederbooms.ccl.kuleuven.be/documentation/manual-EN-POS-CGN.pdf>`_ is used (see ``resource/cgn_to_nt2lex.yaml``).

NT2Lex-CGN+ODWN
   The extended version includes 17,743 entries that have been disabmiguated for word senses with the `SVM-WSD tool <https://github.com/cltl/svm_wsd>`_ trained on DutchSemCor. Each word sense is also linked to its synset in `Open Dutch WordNet <http://wordpress.let.vupr.nl/odwn/>`_.

For each lexical entry, the following linguistic information is given:

- ``word``: the canonical form of the word (lemma)
- ``tag``: the part of speech (simplified CGN tagset)
- ``sense_se-id``: the sense id (if applicable)
- ``sense_sy-id``: the synset id (if applicable)

For each lexical entry appearing at ``@<cefr_level>``, the following corpus statistics are given:

- ``D``: dispersion index
- ``F``: raw frequency
- ``SFI``: standard frequency index
- ``U``: normalized frequency per 1 million words
- ``tf-idf``: term frequency inverse document frequency

Missing values are indicated with a hyphen ``-``.

Tools
-----

- `search the NT2Lex database <https://cental.uclouvain.be/nt2lex/search/>`_
- `analyze the lexical complexity of a text with NT2Lex <https://cental.uclouvain.be/nt2lex/analyse/>`_

Citation
--------

More information can be found in the following `paper <http://aclweb.org/anthology/W18-0514>`_. When using the resource(s) in your research or publication, please cite this paper as well.

.. code-block:: latex
   
   @inproceedings{tack-etal-2018-nt2lex,
      title = {{NT}2{L}ex: A {CEFR}-Graded Lexical Resource for {D}utch as a Foreign Language Linked to Open {D}utch {W}ord{N}et},
      author = {Tack, Ana{\"\i}s  and
         Fran{\c{c}}ois, Thomas  and
         Desmet, Piet  and
         Fairon, C{\'e}drick},
      booktitle = {Proceedings of the Thirteenth Workshop on Innovative Use of {NLP} for Building Educational Applications},
      month = jun,
      year = {2018},
      address = {New Orleans, Louisiana},
      publisher = {Association for Computational Linguistics},
      url = {https://aclanthology.org/W18-0514},
      doi = {10.18653/v1/W18-0514},
      pages = {137--146}
   }

More details can also be found in `Chapter 4 of my Ph.D. thesis <https://dial.uclouvain.be/pr/boreal/object/boreal:248811>`_.

License
-------

This work is licensed under a `Creative Commons
Attribution-NonCommercial-ShareAlike 4.0 International
License <http://creativecommons.org/licenses/by-nc-sa/4.0/>`__.

See LICENSE.txt for more details.


Changelog
---------

All notable changes to this project will be documented in this file.

The format is based on `Keep a Changelog <https://keepachangelog.com/en/1.0.0/>`__,
and this project adheres to `Semantic Versioning <https://semver.org/spec/v2.0.0.html>`__.

[1.0.0] - 2018-06-05
~~~~~~~~~~~~~~~~~~~~

Added
   - First release of the resource

.. |copy|   unicode:: U+000A9 .. COPYRIGHT SIGN