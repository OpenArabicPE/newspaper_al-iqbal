---
title: "newspaper_al-iqbal: read me"
author: Till Grallert
date: 2022-02-02
ORCID: orcid.org/0000-0002-5739-8094
---

This repository contains bibliographic metadata for the private newspaper *al-Iqbāl* published from 9 April 1902 onwards by ʿAbd al-Bāsiṭ al-Unsī in Beirut.

Digital facsimiles are openly accessibly through East Views's [Global Press Archive](https://gpa.eastview.com/crl/mena/newspapers/aliq)

# some technical details

This repository contains the following files:

1. a [TEI XML](metadata/al-iqbal.TEIP5.xml) file containing one `<biblStruct>` for each issue of *al-Iqbāl* between #1 and #280 for which there are digital facsimiles available from East View's [open-access collection](https://www.eastview.com/resources/gpa/crl-mena/) "Global Press Archive". This file was produced through automatic iteration making use of [this code developed for OpenArabicPE](https://github.com/OpenArabicPE/generate_metadata-through-iteration/tree/al-iqbal) and manual validation against the digital facsimiles.
2. individual TEI files for every issue of *al-Iqbāl*. These are generated from the output of step 1 using the XSLT stylesheet [`generate_tei-from-biblstruct.xsl`](https://github.com/OpenArabicPE/generate_metadata-through-iteration/blob/al-iqbal/xslt/generate_tei-from-biblstruct.xsl) from the same repository. TEI files contain links to the local and online facsimiles. A human-readable web interface using a [customisation of the TEI Boilerplate](https://github.com/tillgrallert/tei-boilerplate-arabic-editions) can be accessed [here](https://OpenArabicPE.github.io/newspaper_al-iqbal/tei/oclc_1086411815-i_1.TEIP5.xml).
3. all bibliographic data is then [automatically converted](https://www.github.com/OpenArabicPE/convert_tei-to-bibliographic-data) from TEI XML to MODS XML for integration into reference management software etc (such as Zotero).
4. The TEI files for individual issues were [converted to TSS XML](https://github.com/OpenArabicPE/convert_tei-to-sente/) for use with the now discontinued reference manager Sente. Before import into Sente, one needs to generate one PDF per issue from the attached facsimiles using [this code](https://github.com/OpenArabicPE/generate_pdf-from-attached-facsimiles) and make sure that these files are available (the relative links in TSS XML must be turned into absolute ones).