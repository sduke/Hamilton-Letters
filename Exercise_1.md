# Exercise 1: Data Gathering, Prepping & Cleaning

We will be working with letters from the Founder's Archive website -- the [Hamilton Papers](https://founders.archives.gov/search/Project:%22Hamilton%20Papers%22). 

## Gather Files
1. Download two sets of folders: 
    * [hamilton-all-letters](https://github.com/sduke/Collections-As-Data-Voyant/blob/master/hamilton-all-letters.zip) (compressed files)
    * [hamilton-all-letters_clean](https://github.com/sduke/Collections-As-Data-Voyant/blob/master/hamilton-all-letters_clean.zip) (compressed files)

2. Save both folders to Desktop for easy access

* **If on a Windows machine**, you may need to uncompress the folder before you can open the individual text files. 

## Prepare Files
### Open Files in Text Editor 
1. Launch the Oxygen XML Editor (blue icon with red X).
    * Close the zillions of windows
    * Go to Oxygen XML Preferences => "Encoding"
    * Change Encoding Errors Handling to "IGNORE"
    * Select "OK" in bottom right
 2. In the top menu, select "Project" => "New Project"
 3. In the pop-up:
      * Select the folder on your Desktop: **hamilton-all-letters** 
      * Rename the Project from "newProject.xpr" to "hamilton.xpr". 
 4. Save new Project, "hamilton.xpr," to Desktop 
 
 ### Review Files in Oxygen XML Editor
1. Expand the **hamilton-all-letters** folder (click the arrow next to hamilton-all-letters)
2. Double click on letters of interest to view the fulltext. 
3. To wrap text for readability, select Document in the top menu for each letter you open:
   * Select "Edit" => "Toggle Line Wrap"

# Quick discussion
* What are some potential issues with the text files?

## Clean Files 
* Name normalization 
* Concatenate place names
* Expand abbreviations (_if we have time_)

1. Open **hamilton-all-letters** project in the Oxygen XML Editor
2. In the top menu, select: "Find" => "Find/Replace in Files"
   * In pop-up:
      * Under Text to Find, CHECK "Whole words only"
      * Under Replace with," UNCHECK "Make backup files with extension"
      * Under Scope, SELECT "Project"

### Name Normalization
_We will normalize references to Hamilton's wife, Elizabeth._

#### Elizabeth Hamilton
1. In the top menu, select: "Find" => "Find/Replace in Files"  
2. In "Text to find," search for: 
   * **Mrs. H** 
   * Click "Find All"
   * Review the results
3. In the top menu, select: "Find" => "Find/Replace in Files"
   * In "Text to find," enter **Mrs. H**
   * In the "Replace with," enter **Elizabeth**
   * Click "Replace All ..."
4. Repeat steps 2 & 3 to replace the following names to **Elizabeth**:
   * **Eliza**
   * **Mrs. Hamilton**
   * **Betsey**

#### George Washington
1. In the top menu, select: "Find" => "Find/Replace in Files"  
2. In "Text to find," search for: 
   * **Washington** 
   * Click "Find All"
   * Review the results
3. In the top menu, select: "Find" => "Find/Replace in Files"
   * In "Text to find," enter **Mrs. Washington**
   * In the "Replace with," enter **Martha**
   * Click "Replace All ..."
4. Repeat steps 2 & 3 to replace the following names to:
   * **Mrs. Martha Washington** => **Martha**
   * **His Excellency General Washington** => **Washington**
   * **His Excellency** => **Washington** (note the case insensitivity)

### Concatenate Place Names
_Concatenating compound terms is a quick and easy way to tokenize concepts for text analysis._

1. In the top menu, select: "Find" => "Find/Replace in Files"  
2. In "Text to find," search for: 
   * **Elizabeth Town**
   * Click "Find All"
   * Review the results
3. In the top menu, select: "Find" => "Find/Replace in Files"
   * In "Text to find," enter **Elizabeth Town**
   * In the "Replace with," enter **Elizabeth_Town**
   * Click "Replace All ..."
4. Repeat steps 2 & 3 to replace the following names:
   * **Fort Washington** => **Fort Washington**
   * **New York** => **New_York**
   * **New Jersey** => **New_Jersey**
   * **New England** => **New_England**

### Expand Abbreviations
1. In the top menu, select: "Find" => "Find/Replace in Files"  
2. In "Text to find," search for: 
   * **Obed**
   * Click "Find All"
   * Review the results
3. In the top menu, select: "Find" => "Find/Replace in Files"  
      3. In "Text to find," enter **Obed**
      3. In the "Replace with," enter **Obedient**
      3. Click "Replace All ..."
4. Repeat steps 2 & 3 to replace the following names:
   * **Obdt.** => **Obedient** (_note that same words that contain punctuation need to be removed first_)
   * **Obdt** => **Obedient**
   * **Obt.** => **Obedient**
   * **Obt** => **Obedient**
   * **Serv.** => **Servant**
   * **Serv** => **Servant**
    * **Servt.** => **Servant**
   * **Servt** => **Servant**

## Visualize Files 
* [Original Texts (Unclean) in Voyant](https://voyant-tools.org/?corpus=81e81929a4449f69d83384ac026bc4c0&panels=cirrus,reader,trends,summary,contexts)
* [Cleaned Texts in Voyant](https://voyant-tools.org/?corpus=3d083d30e2d6750dcab2294eda2a46ee&panels=cirrus,reader,trends,summary,contexts) 

