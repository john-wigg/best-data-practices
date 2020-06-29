# Documenting Data: Best Practices

Eine coole Beschreibung, was genau das Ziel dieses Artikels ist.

Die Links zu den Headern in der Checkliste funktionieren so nur auf GitHub vermutlich.

Trick, den ich zum Zitieren benutze:

```
Die Text zitiert eine Quelle [[1]](#cite-example).

<a id="cite-example"></a>[1] <https://github.com/john-wigg/best-data-practices>
```

sieht dann so aus:

Die Text zitiert eine Quelle [[1]](#cite-example).

<a id="cite-example"></a>[1] <https://github.com/john-wigg/best-data-practices>

## Checklist

- [ ] [Metadata standard](#metadata-standard)
- [ ] [Cite your sources](#cite-your-sources)
- [ ] [Choose a license](#choose-a-license)  
- [ ] [File naming](#file-naming)  
- [ ] [Versioning](#versioning)  
- [ ] [Keeping track of processing](#keeping-track-of-processing)  
- [ ] [README](#readme)  
- [ ] [Persistent identifier](#persistent-identifier)

### Metadata standard
This is the most important of the following points:
Use a metadata standard. 
Most points following should already be covered by your chosen standard, so it is a very good idea to pick a standard an then stick to it.
The standard itself should be easily accessible and widely known, at least in your field. If this is not possible, make sure to preserve the scheme itself and its documentation along with your data and metadata.

### Cite your sources

As part of data provenance, researchers need to be able to know from where your data comes. This includes giving information on from where you sourced pre-existing data. [[1]](#cite-fair-provenance-1)

Citing your sources may also be a legal requirement, depending on the license of the work you are citing.

When citing, try to stick to a consistent citation style. Check with people in your field which style to use but use it consistently.

It is also a good idea to make sure that your sources stay accessible long after publication. *Digital Object Identifiers* (DOI, https://www.doi.org/) are persistent identifiers for all kinds of objects such as papers and data sets. Including a DOI, when available, will guarantee permanent access to the cited resource. Otherwise, using web archive sites to capture persistent "snapshots" of webpages can also be an option. Popular providers are [arhive.today](http://archive.today) as well as [Wayback Machine](https://web.archive.org/save). The generated links can then be included with your citations.

***
**REMEMBER**

Cite all your sources consistently and permanently.

***


<a id="cite-fair-provenance-1"></a>[1] <https://www.go-fair.org/fair-principles/r1-2-metadata-associated-detailed-provenance/>


### Choose a license

When opening your project or data to the public, it is important to choose a license. This does not only apply to software projects but really to all kinds of data as well. Without a license, colleagues viewing your publication won't know what they are allowed to with your data and what they aren't.

If publishing in a journals, there may by restrictions on what licenses you are allowed to use so make sure to check with your publisher first.

Licensing may also be a factor when applying the FAIR data principles: To meet the R (Reusable) criteria your *(Meta)data are released with a clear and accessible data usage license* [[1]](#cite-fair-license). The protocol you are using should also be *open, free and universally implementable* so make sure you read the licenses of any component you are using as well. Licensing also makes sure that researcher re-using your data know how to cite you, an important aspect of data provenance in FAIR data [[2]](#cite-fair-provenance-2).

There are good resources to learn about and choose the correct license for your publication https://choosealicense.com/.

A very popular choice are the *Creative Commons* licenses (https://creativecommons.org/licenses/). They allow control of what can be done with your data.

If you are working on a software project, the MIT license is a very clear permissive license. The GNU General Public License is also a very popular choice amongst open-source software projects.

<span style="background-color:red">
 
***
**REMEMBER**

Add a license to your data to tell other researchers what they are allowed to with your data!
***

</span>

<a id="cite-fair-license"></a>[1] <https://www.go-fair.org/fair-principles/r1-1-metadata-released-clear-accessible-data-usage-license/><br>
<a id="cite-fair-provenance-2"></a>[2] <https://www.go-fair.org/fair-principles/r1-2-metadata-associated-detailed-provenance/>

### File naming

* Develop a naming scheme right at the beginning of your project. Stay consistent, if you change your naming scheme, adapt the changes everywhere, even old files.
* Formatting:
  * Avoid spaces.
  * Seperate words by using underscores or use CamelCase.
  * Very long names are problematic for certain software, so avoid.
  * Use leading zeros for sequential numbering.
* Include date in sensible format.
* Use some organisational elements for fast identification such as short name of location.

![Example for bad practice](https://imgs.xkcd.com/comics/documents.png "An example for very bad practice https://xkcd.com/1459/")

### Versioning

If you can, use a version control software like [git](https://git-scm.com/). 
Else, make sure to include version numbers and always keep the information about what changes you made, see also in the [following section](#keeping-track-of-processing).
Things not to put under version control (if you use it):
* Binary files
* Raw data (this should always stay the same!)
* Large data files or results


### Keeping track of processing
It is very important to keep track of all the steps used to process raw data. You can go the easy (and also very good) way of using data-cleaning tools such as [OpenRefine](https://openrefine.org/). It will automatically keep track of your changes and has some other cool features.
Another option is writing a script that does all the necessary changes for you. This is also useful if you get more new data which needs to be processsed the same way as the old.
If neither of this options suits you, you could write log messages or keep track of the changes in a README. Make sure to use [version control](#versioning), especially for files that you edit manually. 

### README

Keep a README or something similar in your file folders to give other users of your data (or yourself) a better overview. Metadata you could include:
* Subject: Describe the content of your data in keywords or short sentences
* Place: Include the physical locations of your data collection
* Languages: Mention all languages used in your data
* Variable List: Describe the variables used in the data files
* Code list: Explain the abbreviations used in your project
* Null character: Specify which Null character you used

### Persistent identifier

Use a persistent Digital identifier for your project (DOI) as well as for yourself (e.g. [ORCID](https://orcid.org/)).
They will help your project in staying findable, accesible and connected to you.
