+++
title = 'Vsxmd'
date = 2020-08-28T23:20:13.2033008+10:00
+++
## Contents
- [Converter](#converter-type)
  - [Constructor(document)](#constructordocument-method)
  - [ToMarkdown(document)](#tomarkdowndocument-method)
  - [ToMarkdown()](#tomarkdown-method)
- [IConverter](#iconverter-type)
  - [ToMarkdown()](#tomarkdown-method)
- [Program](#program-type)
  - [Main(args)](#mainargs-method)
- [TableOfContents](#tableofcontents-type)
  - [Constructor(memberUnits)](#constructormemberunits-method)
  - [ToMarkdown()](#tomarkdown-method)
## Converter `type`

*Inherit from parent.*
### Constructor(document) `method`

Initializes a new instance of the [Converter](#converter-type 'Vsxmd.Converter') class.
##### Parameters
| Name | Type | Description |
| ---- | ---- | ----------- |
| document | [System.Xml.Linq.XDocument](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.Xml.Linq.XDocument 'System.Xml.Linq.XDocument') | The XML document. |
### ToMarkdown(document) `method`

Convert VS XML document to Markdown syntax.
##### Returns
The generated Markdown content.
##### Parameters
| Name | Type | Description |
| ---- | ---- | ----------- |
| document | [System.Xml.Linq.XDocument](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.Xml.Linq.XDocument 'System.Xml.Linq.XDocument') | The XML document. |
### ToMarkdown() `method`

*Inherit from parent.*
##### Parameters
This method has no parameters.
## IConverter `type`

Converter for XML document to Markdown syntax conversion.
### ToMarkdown() `method`

Convert to Markdown syntax.
##### Returns
The generated Markdown content.
##### Parameters
This method has no parameters.
## Program `type`

Program entry.
##### Remarks
Usage syntax:

```
Vsxmd.exe &lt;input-XML-path&gt; [output-Markdown-path]
```

The `input-XML-path` argument is required. It references to the VS generated XML documentation file.

The `output-Markdown-path` argument is optional. It indicates the file path for the Markdown output file. When not specific, it will be a `.md` file with same file name as the XML documentation file, path at the XML documentation folder.
### Main(args) `method`

Program main function entry.
##### Parameters
| Name | Type | Description |
| ---- | ---- | ----------- |
| args | [System.String[]](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.String[] 'System.String[]') | Program arguments. |
##### See Also
- [Vsxmd.Program](#program-type 'Vsxmd.Program')
## TableOfContents `type`

Table of contents.
### Properties 
|Name|Description|
| ---- | ---- |
|Link|Gets the link pointing to the table of contents.|
### Constructor(memberUnits) `method`

Initializes a new instance of the [TableOfContents](#tableofcontents-type 'Vsxmd.TableOfContents') class.

It convert the table of contents from the `memberUnits`.
##### Parameters
| Name | Type | Description |
| ---- | ---- | ----------- |
| memberUnits | [System.Linq.IOrderedEnumerable{Vsxmd.Units.MemberUnit}](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.Linq.IOrderedEnumerable 'System.Linq.IOrderedEnumerable{Vsxmd.Units.MemberUnit}') | The member unit list. |
### ToMarkdown() `method`

Convert the table of contents to Markdown syntax.
##### Returns
The table of contents in Markdown syntax.
##### Parameters
This method has no parameters.
