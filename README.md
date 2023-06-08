# Notion-2-Obsidian

For those considering switching from [Notion](https://www.notion.so/) to [Obsidian](https://obsidian.md/), here is a Python 3 script that converts your Notion export into an Obsidian friendly format. 

When you run the N2O.py script, it will:
1. Require you to launch from command line with command 
```shell
python N2O.py -i notion-export.zip
```
2. Convert all Internal Links in your Notion pages to an Obsidian friendly markdown format
3. Repackages all the files into a new zip archive that is Obsidian vault compatible
4. Output the zip file to the output directory

The script will leave your orginal Notion archive unmodified. 

The resulting archive can be extracted and opened as, or added to, an Obsidian vault.

## The Problem with your Notion Export
Out of the box, the export files that Notion provides do not migrate to Obsidian very well. All external links will work, but:

- The hierarchical structure of your pages can only be navigated using Obsidian’s file explorer. 
- None of the internal navigation links work, which also means there won’t be any backlinks or connections in Obsidian's Graph View. 
- None of the content in your Notion tables will be viewable.  
- Embedded images also won’t show. 

All of this is remedied by this script. Note however, that Notion comments do NOT appear to be included in their export files.

## Methodology

If you're interested, the full sequence of modifications needed to make your Notion export compatible with Obsidian can be found in the write-up found in the [Methodology.md](METHODOLOGY.md) file in this git.

# Supporting the Work

Credit to: [visual current](https://github.com/visualcurrent)

# Export Your Full Notion Database
If you haven't already, you'll need to export your content from Notion.

1.  From your Notion app, click the **Settings & Members** tab in the sidebar  
![Settings&Members](media/export1.png)
2.  Find and click the **Settings** tab. Find the **Export content** section. Click the **Export all workspace content** button  
![Settings](media/export2.png)
3.  Select **Markdown & CSV** as Export Format and click the **Export** button  
![Export](media/export3.png)
4.  Save the resulting .zip file to your computer
5.  Extract the .zip contents to a known location

# Run the N2O.py Script
- Make sure `N2O.py` and `N2Omodule.py` are in the same directory.
- Run `Python3 N2O.py`
- Use the Open-File dialog that pops up to navigate to your NotionExport.zip file.
- When the script finishes you'll find a new zip file in the same directory that's ready for Obsidian.

# Importing or Integrating into Obsidian

Time to import everything into Obsidian

1.  Place all the converted files into a directory of your choosing
2.  Open Obsidian and click the Vault Icon ![vault icon](media/vaulticon.png)
3.  Select **Open folder as vault**  
![open vault](media/vault.png)
4.  Use the Select Folder window to navigate to the directory with your newly converted files
