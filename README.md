# 4d-plugin-pdf-document-attributes
A small subset of [PDFKit](https://developer.apple.com/documentation/pdfkit?language=objc) to access basic properties of the [PDFDocument](https://developer.apple.com/documentation/pdfkit/pdfdocument?language=objc) class.

## Platform

| carbon | cocoa | win32 | win64 |
|:------:|:-----:|:---------:|:---------:|
|<img src="https://cloud.githubusercontent.com/assets/1725068/22371562/1b091f0a-e4db-11e6-8458-8653954a7cce.png" width="24" height="24" />|<img src="https://cloud.githubusercontent.com/assets/1725068/22371562/1b091f0a-e4db-11e6-8458-8653954a7cce.png" width="24" height="24" />|||

### Version

<img src="https://cloud.githubusercontent.com/assets/1725068/18940649/21945000-8645-11e6-86ed-4a0f800e5a73.png" width="32" height="32" /> <img src="https://cloud.githubusercontent.com/assets/1725068/18940648/2192ddba-8645-11e6-864d-6d5692d55717.png" width="32" height="32" />

### Compatibility Note

This plugin shared the same command name and constants as [pdf-kit](https://github.com/miyako/4d-plugin-pdf-kit), but the signature and data types are incompatible; therefore you can not use both together. First, comment out the old code, replace the plugin, then uncomment the code to complete the transition.

---

## Syntax

```
PDF GET DOCUMENT ATTRIBUTES (path;attributes;values)
PDF SET DOCUMENT ATTRIBUTES (path;attributes;values)
```

Parameter|Type|Description
------------|------------|----
path|TEXT|
attributes|ARRAY LONGINT|see constants below
values|ARRAY TEXT|

For the ``GET`` command, a ``JSON`` is returned in element ``0`` of ``values``.

For ``PDF_KEYWORDS`` the delimiter is a ``,``.

### Constants

* From ``PDFDocumentAttribute``

```
PDF_TITLE PDFDocumentTitleAttribute 1
PDF_AUTHOR PDFDocumentAuthorAttribute 2
PDF_SUBJECT PDFDocumentSubjectAttribute 3
PDF_CREATOR PDFDocumentCreatorAttribute 4
PDF_PRODUCER PDFDocumentProducerAttribute 5
PDF_KEYWORDS PDFDocumentKeywordsAttribute 6
PDF_CREATION_DATE PDFDocumentCreationDateAttribute 7 
PDF_MODIFICATION_DATE PDFDocumentModificationDateAttribute 8
```

* Properties (read only)

```
PDF_PAGE_COUNT pageCount 9
PDF_MAJOR_VERSION majorVersion 10
PDF_MINOR_VERSION minorVersion 11
PDF_ALLOWS_PRINTING allowsPrinting 12
PDF_ALLOWS_COPYING allowsCopying 13
PDF_IS_LOCKED isLocked 14
PDF_IS_ENCRYPTED isEncrypted 15
PDF_PERMISSIONS permissionsStatus 16
```

* Not supported (added in 10.13 SDK)

```
allowsCommenting
allowsContentAccessibility
allowsDocumentAssembly
allowsDocumentChanges
allowsFormFieldEntry
```
