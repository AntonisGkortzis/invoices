invoices
========

Generates invoices to be used according to the latest (2012-2013) tax regulations.

Usage
=====

    python invoice.py invoice.xml
    xelatex invoice_<num>.tex

where `invoice.xml` is a file containing the data to be entered in a particular invoice. The data are contained in
the following elements:

* num: the invoice number; this number will be used to produce the output filename `invoice_<num>.tex` and to number
  the invoice itself
* date: the invoice date
* stamp: the boilerplate that is usually present in the traditional invoice stamps
* client: the client name
* occupation: the client occupation
* taxoffice: the client tax office
* address: the client address
* taxnumber: the client taxnumber
* description: the description of the work performed
* value: the value of the work performed; this is the only amount that needs to be entered, as the tax, the VAT, as well 
  the string representation of the amount are produced automatically, except if a vat element is present
* vat: if present, the value of VAT to be used; useful in cases where VAT is not to be levied at all

A sample `invoice.xml` is included in the repo, as is an [example output](https://github.com/louridas/invoices/blob/master/invoice_1.pdf).
