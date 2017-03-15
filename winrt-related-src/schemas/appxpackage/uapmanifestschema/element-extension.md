---
Description: Extension (in Package/Extensions) (Windows 10)
MS-HAID: UapManifestSchema.element\_Extension
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/apps
Search.Product: eADQiWindows 10XVcnh
title: Extension (in Package/Extensions) (Windows 10)
ms.assetid: 72f0d1ae-15a4-4eba-a3ca-990f4de2b697
author: laurenhughes
ms.author: lahugh
keywords: windows 10
---

# Extension (in Package/Extensions) (Windows 10)


Declares an extensibility point for the package.

## Element hierarchy

<dl>
<dt><a href="element-package.md">&lt;Package&gt;</a></dt>
<dd>
<dl>
<dt><a href="element-extensions.md">&lt;Extensions&gt;</a></dt>
<dd><b>&lt;Extension&gt;</b></dd>
</dl>
</dd>
</dl>

## Syntax

``` syntax
<Extension Category = "windows.activatableClass.inProcessServer" | "windows.activatableClass.outOfProcessServer" | "windows.activatableClass.proxyStub" | "windows.certificates" | "windows.publisherCacheFolders" >

  <!-- Child elements -->
  ( InProcessServer
  | OutOfProcessServer
  | ProxyStub
  | Certificates
  | PublisherCacheFolders
  )

</Extension>
```

## Attributes and Elements


### Attributes

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th>Attribute</th>
<th>Description</th>
<th>Data type</th>
<th>Required</th>
<th>Default value</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Category</strong></td>
<td><p>The type of package extensibility point.</p></td>
<td><p>This attribute can have one of the following values:</p>
<ul>
<li>windows.activatableClass.inProcessServer</li>
<li>windows.activatableClass.outOfProcessServer</li>
<li>windows.activatableClass.proxyStub</li>
<li>windows.certificates</li>
<li>windows.publisherCacheFolders</li>
</ul></td>
<td>Yes</td>
<td></td>
</tr>
</tbody>
</table>

 

### Child Elements

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Child Element</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>[Certificates](element-certificates.md)</td>
<td><p>Declares a package extensibility point of type <strong>windows.certificates</strong>. The app requires one or more certificates from the specified certificate stores.</p></td>
</tr>
<tr class="even">
<td>[InProcessServer](element-inprocessserver.md)</td>
<td><p>Declares a package extensibility point of type <strong>windows.activatableClass.inProcessServer</strong>. The app uses a dynamic link library (DLL) that exposes one or more activatable classes.</p></td>
</tr>
<tr class="odd">
<td>[OutOfProcessServer](element-outofprocessserver.md)</td>
<td><p>Declares a package extension point of type <strong>windows.activatableClass.outOfProcessServer</strong>. The app uses an executable (EXE) that exposes one or more activatable classes.</p></td>
</tr>
<tr class="even">
<td>[ProxyStub](element-proxystub.md)</td>
<td><p>Declares a package extensibility point of type <strong>windows.activatableClass.proxyStub</strong>. A proxy can be composed of one or more interfaces.</p></td>
</tr>
<tr class="odd">
<td>[PublisherCacheFolders](element-publishercachefolders.md)</td>
<td><p>Declares a package extensibility point of type <strong>windows.publisherCacheFolders</strong>. This specifies one or more folders that the package shares with other packages from the same publisher.</p></td>
</tr>
</tbody>
</table>

 

### Parent Elements

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Parent Element</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>[Extensions (type: CT_PackageExtensions)](element-extensions.md)</td>
<td><p>Defines one or more extensibility points for the package.</p></td>
</tr>
</tbody>
</table>

 

## Related elements


The following elements have the same name as this one, but different content or attributes:

-   **[Extension (global)](element-1-extension.md)**

## Remarks

Extensibility points are a mechanism by which a package can add functionality in a manner defined by the operating system. An extensibility point is a location where an app can register to execute code or use resources of the current package. To add functionality for a particular app, use the [**Application**](element-application.md) child element of the [**Applications**](element-applications.md) element.

The **windows.certificates** extensibility point can't be declared multiple times in a manifest.

## See also


**Concepts**
[App contracts and extensions](https://msdn.microsoft.com/library/windows/apps/hh464906)

## Requirements

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Namespace</p></td>
<td><p>http://schemas.microsoft.com/appx/manifest/foundation/windows10</p></td>
</tr>
</tbody>
</table>

 

 


