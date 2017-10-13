# 4d-plugin-pdf-document-attributes
A small subset of [PDFKit](https://developer.apple.com/documentation/pdfkit?language=objc) to access basic properties of the [PDFDocument](https://developer.apple.com/documentation/pdfkit/pdfdocument?language=objc) class.

## Platform

| carbon | cocoa | win32 | win64 |
|:------:|:-----:|:---------:|:---------:|
|<img src="https://cloud.githubusercontent.com/assets/1725068/22371562/1b091f0a-e4db-11e6-8458-8653954a7cce.png" width="24" height="24" />|<img src="https://cloud.githubusercontent.com/assets/1725068/22371562/1b091f0a-e4db-11e6-8458-8653954a7cce.png" width="24" height="24" />|<img src="https://cloud.githubusercontent.com/assets/1725068/22371562/1b091f0a-e4db-11e6-8458-8653954a7cce.png" width="24" height="24" />|<img src="https://cloud.githubusercontent.com/assets/1725068/22371562/1b091f0a-e4db-11e6-8458-8653954a7cce.png" width="24" height="24" />|

### Version

<img src="https://cloud.githubusercontent.com/assets/1725068/18940649/21945000-8645-11e6-86ed-4a0f800e5a73.png" width="32" height="32" /> <img src="https://cloud.githubusercontent.com/assets/1725068/18940648/2192ddba-8645-11e6-864d-6d5692d55717.png" width="32" height="32" />

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

For the ``GET`` command, a ``JSON`` is returned in element ``0``.

### Constants

* From ``PDFDocumentAttribute``

```
PDF_TITLE PDFDocumentTitleAttribute
PDF_AUTHOR PDFDocumentAuthorAttribute
PDF_SUBJECT PDFDocumentSubjectAttribute
PDF_CREATOR PDFDocumentCreatorAttribute
PDF_PRODUCER PDFDocumentProducerAttribute
PDF_KEYWORDS PDFDocumentKeywordsAttribute
PDF_CREATION_DATE PDFDocumentCreationDateAttribute 
PDF_MODIFICATION_DATE PDFDocumentModificationDateAttribute
```

* Properties (read only)

```
PDF_PAGE_COUNT pageCount
PDF_MAJOR_VERSION majorVersion
PDF_MINOR_VERSION minorVersion
PDF_ALLOWS_PRINTING allowsPrinting
PDF_ALLOWS_COPYING allowsCopying
PDF_IS_LOCKED isLocked
PDF_IS_ENCRYPTED isEncrypted
PDF_PERMISSIONS permissionsStatus
```

* Nupported (added in 10.13 SDK)

```
allowsCommenting
allowsContentAccessibility
allowsDocumentAssembly
allowsDocumentChanges
allowsFormFieldEntry
```
