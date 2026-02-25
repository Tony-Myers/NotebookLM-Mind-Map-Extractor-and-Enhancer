# NotebookLM Mind Map Extractor and Enhancer

A self-contained, offline-friendly web application designed to extract, build, and enhance interactive mind maps. It allows users to pull mind map structures directly from Google NotebookLM, expand them with rich media and documents, and export the result as a single, portable HTML file.

## Core Features

* **NotebookLM Extraction:** Includes a custom browser bookmarklet that reads the underlying D3.js data bindings (OPML) directly from a NotebookLM page.
* **Visual Builder:** Construct and edit mind maps from scratch using an intuitive graphical interface and standard keyboard shortcuts.
* **Rich Attachments:** Embed images, web links, and full documents (PDF, Word, Excel, PowerPoint) directly into individual nodes. Files are base64-encoded, ensuring the exported map remains completely self-contained.
* **OPML Support:** Import existing OPML/XML files or export your current map to OPML for use in other personal knowledge management (PKM) software.
* **Multiple Visualisations:** Render the final interactive map in three distinct D3.js layouts: Left-to-Right tree, Top-to-Bottom tree, or Radial.
* **Zero Dependencies:** The generator is a single HTML file. It does not require a database, backend server, or active internet connection to function (aside from the initial D3.js library load in the exported file).

## Getting Started

### 1. Installation
There is no installation required. Simply download the `index.html` file (or host it via GitHub Pages) and open it in any modern web browser.

### 2. Extracting from NotebookLM
1. Open the generator and navigate to the **NotebookLM Import** tab.
2. Drag the **Extract NotebookLM Map** button to your browser's bookmarks bar.
3. Open a Google NotebookLM notebook that contains a visible mind map.
4. Click the bookmarklet in your bookmarks bar. The map structure will be copied to your clipboard as OPML code.
5. Return to the generator, paste the OPML code into the designated text area, and click **Load into Visual Builder**.

### 3. Building and Enhancing
* Navigate to the **Visual Builder** tab to add siblings or children to your nodes.
* Double-click any node to rename it.
* Select a node and use the attachment buttons to embed images or documents. Do note that embedding large documents will proportionately increase the final export file size.

### 4. Exporting
Once you have finished customising your map, select your preferred default layout from the drop-down menu and click **Download interactive mind map**. The tool will generate a new HTML file that you can save locally, share with colleagues, or host directly on a web server.

## Technical Details

This tool is built entirely with vanilla HTML, CSS, and JavaScript. It utilises [D3.js](https://d3js.org/) to render the interactive mind map visualisations in the exported files. All application states are saved automatically in your browser's `localStorage` to prevent accidental data loss during sessions.

## Disclaimer

This project is an independent utility and is not officially affiliated with, endorsed by, or connected to Google or the NotebookLM team. The extraction bookmarklet relies on the current DOM structure of NotebookLM and may require updates if the underlying architecture changes.
