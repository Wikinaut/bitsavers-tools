# bitsavers-tools
Tools for submitting scanned data books in the correct format to http://bitsavers.org


### [make-tifpdf](https://github.com/Wikinaut/bitsavers-tools/blob/main/make-tifpdf) input.pdf [output.pdf]

a script for converting one pdf with scanned pages (300-600 dpi, color or grey)   
to a PDF with

* 600 dpi 1-bit TIFF pages
* optionally (default) colored 300 dpi jpg front/cover pages.


### Usage example

```
$ ./make-tifpdf 1973_Fairchild_Semiconductor_The_TTL_Applications_Handbook_197308.pdf 
Processing:
1,2G 1973_Fairchild_Semiconductor_The_TTL_Applications_Handbook_197308.pdf
372 PDF pages
Progress : [########################################] 100%
1,2G done/1973_Fairchild_Semiconductor_The_TTL_Applications_Handbook_197308.pdf.done
75M tumble/1973_Fairchild_Semiconductor_The_TTL_Applications_Handbook_197308--tumble--600dpi.pdf

=== Summary ===
Colored front/back cover: yes
1062.43 seconds processing time
PDF: 372 pages
21.00 pages/minute
2.85 seconds/page
```

![grafik](https://user-images.githubusercontent.com/1151915/214706285-f79cad1c-f270-4e86-83be-2652aff87fbe.png)

### Requirements

* pdftoppm
* convert (part of Imagemagick)
* tumble https://github.com/brouhaha/tumble is a utility by Eric Smith to construct an PDF file from one (or more) 1-bit-tiff image files and/or jpg files.
