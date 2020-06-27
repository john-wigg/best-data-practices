# Documenting Data: Best Practices

Eine coole Beschreibung, was genau das Ziel dieses Artikels ist.

Die Links zu den Headern in der Checkliste funktionieren so nur auf GitHub vermutlich.

## Checklist

[Metadata standard](#metadata-standard)  
[Licence](#licence)  
[File naming](#file-naming)  
[Versioning](#versioning)  
[Keeping track of processing](#keeping-track-of-processing)  
[README](#readme)  
[Persistent identifier](#persistent-identifier)

### Metadata standard
This is the most important of the following points:
Use a metadata standard. 
Most points following should already be covered by your chosen standard, so it is a very good idea to pick a standard an then stick to it.
The standard itself should be easily accessible and widely known, at least in your field. If this is not possible, make sure to preserve the scheme itself and its documentation along with your data and metadata.

### Licence

Pick a license that's well suited for your project.

For open source projects, this site seems to be informative: https://choosealicense.com/

A very popular and very permissive license is the MIT License.

Creative Commons Licenses may also be a good choice since they allow you to control what rights you want to retain: https://creativecommons.org/licenses/

### File naming

* Develop a naming scheme right at the beginning of your project. Stay consistent, if you change your naming scheme, adapt the changes everywhere, even old files.
* Formatting:
  * Avoid spaces.
  * Seperate words by using underscores or use CamelCase.
  * Very long names are problematic for certain software, so avoid.
  * Use leading zeros for sequential numbering.
* Include date in sensible format.
* Use some organisational elements for fast identification such as short name of location.

![Example for bad practice](https://imgs.xkcd.com/comics/documents.png (An example for very bad practice https://xkcd.com/1459/))

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
