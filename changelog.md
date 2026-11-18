# PDFix Desktop changelog

# PDFix Desktop

## [4.0.0] - 2026-11-18

### Highlights

PDFix Desktop 4.0 brings full support for PDF 2.0 and PDF/UA-2, a workspace you can arrange the way you like, and new ways to see your document the way assistive technology does. A new validation score shows how much accessibility work is left, and large tagged documents now save and edit noticeably faster.

- **Arrange your workspace.** Move, tab, and float panes, pick a named theme, and scale the interface independently of your system settings.
- **See what screen-reader users experience.** The new Screen Reader view in the Tags pane and the Reading view for HTML output show your document's structure the way assistive technology reads it.
- **Know how much work is left.** Validation automatically checks against the PDF/UA version declared in the file, and the new validation score estimates the remaining effort. PDF/UA compliance itself is still a clear Pass or Fail.
- **New conversion and tagging tools.** Convert to Markdown and EPUB, tag text with search patterns, wrap and repair tags, split and insert pages, and fix PDF/UA-2 issues with dedicated actions.
- **Faster, safer saving.** Incremental save, faster saving of large tagged files, and a progress bar with Cancel for long saves.
- **Stay up to date.** PDFix Desktop can now update itself from within the app.

### Workspace and User Interface

**New**
- Move, tab, and float panes in both App View and Document View. Use Reset Layout to restore the default arrangement at any time.
- Choose from named themes and set the interface scale separately from your system.
- A new status bar shows your license, document security, PDF version, and the PDF standards the file claims to meet.
- Reading view: open an easy-to-read HTML version of your document directly from Document View, with a table of contents and a screen-reader-style view of the tag structure. You can set it as your default in Preferences.
- Search in HTML and Reading view with the same Ctrl+F shortcut as in the PDF view. The Find panel stays open while you work.
- Find Action is now a dialog under Find, with settings, navigation, and helpful tooltips.
- The action picker is easier to use: search, browse by category, mark favorites, and drag actions straight onto the ribbon.
- The Action pane now works as a draft editor, consistent with Edit and New, and is available from the ribbon, menus, and import.
- A quality bar in App View and Document View shows the validation score at a glance. Click it to see a summary.
- An untagged document now shows a helpful empty state in the Tags pane instead of a blank pane.
- An empty batch now shows a short introduction, a drop area, and an Add Files button.
- File batches appear in a navigation panel on the left, and column widths stay aligned across batches.
- Set a default output file suffix from the Dashboard.
- PDFix Desktop can now update itself. An update button appears in App View, and beta builds check for updates automatically.

**Fixed**
- New batches now use the default columns set on the Dashboard.
- The security status is shown correctly when you open a document with the owner password and it also has a separate permissions password.
- Fit Page no longer jumps when you click.
- Pane highlights no longer shift when you resize the window in Fit Page or Fit Width.
- The Screen Reader view no longer flickers when you use Expand All or when the layout changes.
- Selecting items in tree views now works correctly on macOS.
- Drop-down lists now work correctly on the latest macOS versions.
- Changing the theme no longer marks your layout template as modified.
- Pipeline progress messages no longer show garbled characters.
- Property editors no longer apply changes while you are still typing or when you use Save As. Keyboard shortcuts now keep working after you save in Document View.
- After you hide the Action pane, you can bring it back from the More menu.
- Help icons in menus now keep the correct size.
- In shortcut preferences, clicking a row now selects the whole row.
- The text cursor no longer gets stuck on the HTML view ribbon.
- Save As now opens in the last folder you used.
- Double-clicking in the action picker no longer selects several actions.

### Accessibility and Tagging

**New**
- Screen Reader view in the Tags pane: see your tags as nested boxes, with table spans, image previews, and role mapping, and rearrange or rename tags with drag and drop.
- Edit PDF 2.0 namespaces in the Tags pane and in actions.
- Set or clear a link target that points to a structure element (GoTo structure destination) from the Actions pane or the clipboard.
- **Tag Text:** find text with a search pattern (regular expression) and tag every match, for example as Span, Em, Strong, or your own tag type.
- **Wrap Tags:** add a new parent tag around every tag that matches your criteria.
- **Fix Tag Tree:** repair broken links between tags and page content, keep content names in sync with tag types, and rebuild the internal structure index.
- **Tag as TOC:** recognize and tag a table of contents, including tables of contents laid out with title and page-number columns.
- When you tag content that already belongs to a tag, the new tag is placed inside that existing tag.
- **Split Pages:** split a document by page numbers, tags, or content. Each resulting file keeps its PDF/UA identification.
- **Insert Pages:** after you insert pages, Document View fully refreshes so the page count, thumbnails, and page view stay accurate.
- **Update Form XObjects:** give each placement of a reusable graphic its own copy, so you can tag each one separately. You can also copy its resources and mark the graphic as atomic.
- **Remove Content Properties:** clear alternate text, actual text, language, or abbreviation expansions from page content.
- Select, tag, and highlight repeated graphics (Form XObjects) individually, including graphics that come from annotations.

**Fixed**
- Find Tag from Selection now scrolls to the right place in Screen Reader view.
- Spaces are no longer cut off in the Content pane.
- After you create a span, selection jumps to the parent paragraph as expected.
- Tagging no longer removes transparency from page content.
- Tag As now works when the selected object is a graphic (Form XObject) that carries the content reference.
- Tables whose rows continue across a page break are now handled correctly.
- Set Content Color no longer removes the lines that separate table rows and columns.
- The Hand tool now follows PDF 2.0 structure destinations first when you click a link.

**Removed**
- Fix Invalid Elements has been removed. Use Fix Tag Tree instead.

### Actions and Workflows

**New**
- Run custom actions on just the current selection.
- Export and import an action together with its presets, so you can share complete workflows.
- Create your own action category directly in the action picker.
- Rename individual steps inside a custom compound action.
- Add conditions to individual steps of a custom action, so a step runs only when needed.
- Convert PDF to Markdown and PDF to EPUB.
- Better HTML, Markdown, and EPUB output for lists, tables of contents, forms, and figures.
- Untagged documents now convert to responsive HTML instead of producing empty output.
- New actions that fix PDF/UA-2 issues: descriptions for attached files, file-attachment relationships, caption position, private-use characters in tags and annotations, rich text in form fields, footnotes and endnotes, table-of-contents references, structure link targets, MathML for formulas, and showing the document title in the window title bar.
- Convert Word documents to PDF.
- Move files to the Trash directly from App View, also with Ctrl+Delete.
- All new actions are included in the action categories and in action protection.

**Fixed**
- Converting to HTML, JSON, or EPUB from Document View now asks where to save the result.
- You can now delete a custom action that is marked as a favorite.
- Custom actions can now be renamed in Document View.
- Error messages are clearer when an action fails on a secured document.
- You can now cancel queued batch jobs in App View.
- Validation is offered only for files that are not currently being processed.
- AutoTag Preflight stays visible and enabled when AutoTag runs with a document template.
- Closing the dialog now cancels a conversion in Document View.
- In batches, output from external actions is no longer overwritten, and pipeline reports stay readable.
- Move to Trash now works on Windows even when the PDF is open in preview, and asks for confirmation first.
- Removed actions are also removed from the quick-access ribbon.
- Deleting the last step no longer resets your draft in the Action pane.
- Save to is now shown for the selected custom step.

### Validation

**New**
- Validation now checks against the PDF/UA version declared in the document by default, and that choice stays selected on the ribbon.
- **Validation score:** see how much accessibility work is left, based on the number and kinds of remaining issues. You can see it as a quality bar in the file list and on the open document, or switch to a simple Pass / Fail view. PDF/UA compliance itself remains Pass or Fail.
- Create your own validation scores in Settings → Validation → Validation score. Set a weight for each rule (weight 0 ignores the rule), adjust sensitivity, and import or export your settings.
- Guidance overlays and field display options help you understand and fix validation issues in context.
- veraPDF 1.30.4 is now built in, so no separate installation is needed. It includes a PDF Accessibility profile that also checks WCAG color contrast.
- Revalidate with the profile you are already using. Its name is shown on the status bar.
- The veraPDF version and license are now listed in About.
- The validation action is updated to version 1.4.2 and includes the PDF Accessibility profile.

**Fixed**
- MathML rules show the correct formula icon.
- Font-related PDF/UA-2 errors show the correct action icons.
- Document View stays responsive when you select thousands of validation results. Show Errors now selects results on the visible pages only and highlights the page you are previewing.
- Validation annotations are found on the page correctly.
- Pages appear in the correct order in the Validation panel.
- Save As works when exporting a validation report.
- Exporting a validation report now uses the correct default options.

### Templates and Layout Recognition

**New**
- The template preview highlights on the page the tags and annotations that a template rule matches.
- Edit the layout template directly as plain JSON.
- Compare fill and stroke colors in template rules.
- Turn underline and strikeout detection on or off separately.
- Use page orientation (portrait or landscape) as a template condition.
- Edit start and end bounding boxes.
- The template Add menu is organized into submenus, including Graphics Table and Text Table.
- Element colors in the page map now match the default tag colors.

**Fixed**
- Start and end bounding-box lines are highlighted correctly in the template.
- AutoTag no longer removes role-map entries.
- Missing aliases have been restored in the Document Layout Template.
- Layout recognition data is cleaned up properly when you close a document.

### General

**New**
- Incremental save: only your changes are written, which makes saving faster.
- Long saves show progress and can be canceled.
- Copy and paste object references in the Browser tree.
- Save a stream object to a file from the Browser pane.
- Faster saving and smoother editing of documents with large tag trees.
- Built on [PDFix SDK 10.0.0](https://github.com/pdfix/pdfix_sdk_builds/blob/main/changelog.md#1000---2026-11-18).

## [3.3.0] - 2026-08-31

### Summary

Minor update focused on more reliable Tag and Content pane editing, plus core SDK fixes for PDF/UA metadata, PDF/A save, and tagging actions.

### User Interface

- Fixed Shift+arrow multi-select in tree views on macOS
- Fixed deselecting items when holding Shift while navigating tags at the same level

### Accessibility and Tagging

- Fixed loading content for tags that span multiple pages
- Fixed Move Child leaving a page reference on an ancestor instead of the direct parent of moved content
- Fixed Fix Invalid Elements treating page marked-content kids as orphans
- Fixed Remove Invalid MCID missing page marks

### Actions and Workflows

- Fixed Set Annotation Contents skipping on-page link annotations with a zero-size rectangle

### Metadata and Document Information

- Fixed Set PDF/UA and Fix Metadata wiping existing properties when XMP Metadata is UTF-16 or UTF-32
- Fixed saving PDF/A without object streams or cross-reference streams
- Fixed preserving compact XMP attributes, writing ISO 8601 dates, and declaring the pdfuaid extension schema when setting PDF/UA
- Fixed Dublin Core text properties being wrapped as a bag instead of a single value

### General Updates

- Updated to [PDFix SDK 9.3.0](https://github.com/pdfix/pdfix_sdk_builds/blob/main/changelog.md#930---2026-08-29)

## [3.2.0] - 2026-08-13

### Summary

This release focuses on new tagging and form-font actions, clearer template editing, and more reliable Windows licensing.

### User Interface

- Fixed false unsaved-changes prompt when editing template values

### Accessibility and Tagging

- Added Merge Tags action
- Added Fix Fonts for Form Filling action
- Fixed continuous table tagging across pages
- Fixed graphic table detection
- Fixed Fix Content Marks removing valid Form XObject MCIDs with Remove Invalid MCID

### Actions and Workflows

- Registered Merge Tags in action categorization and protection
- Registered Fix Fonts for Form Filling in action UI, action categorization, and protection
- Fixed AutoTag Preflight — shown in the action; skipped when a template is set

### Templates and Layout Recognition

- Added `tag_neighbours` template function for Merge Tags pair rules (cross-page, Note chains)
- Added `object_num` on structure tags to identify associated page objects
- Added template keyword aliases for Tag Neighbours, Initial Element Expand Overlap, Is Standard Tag, RD Overlap Min Ratio, and Split Filling

### License Management

- Fixed Device ID generation failure using WMI on Windows

### Performance and Stability

- Improved action execution performance

### General Updates

- Updated to [PDFix SDK 9.2.0](https://github.com/pdfix/pdfix_sdk_builds/blob/main/changelog.md#920---2026-08-13)
- Fixed Catalog XMP metadata wrapping in xpacket

## [3.1.1] - 2026-07-16

### Summary

Minor update focused on more reliable action and validation error reporting, plus core SDK fixes for Make Accessible.

- Improved reporting of failed actions and veraPDF single-process error messages.
- Fixed parsing of pipeline STATUS JSON when output is mixed with error messages.
- Updated to PDFix SDK 9.1.1, including a Make Accessible fix for mirrored text with negative horizontal scale.

### Actions and Workflows

- Fixed actions incorrectly reported as failed when the process exit code is non-zero
- Fixed loading of pipeline STATUS JSON when output is mixed with error messages

### Validation and veraPDF

- Updated veraPDF validation action to v1.2.2
- Added all veraPDF single-process error messages

### Accessibility and Tagging

- Fixed Make Accessible mirroring text on the page when horizontal scale is negative

### General Updates

- Updated to [PDFix SDK 9.1.1](https://github.com/pdfix/pdfix_sdk_builds/blob/main/changelog.md#911---2026-07-16)

## [3.1.0] - 2026-06-23

### Summary

This release focuses on stronger accessibility tagging workflows, improved font and validation tooling, and better stability on large structure trees.

- Added new tagging and font actions, including Set Unicode for Font Charcode, Fix Invalid Elements, Set Annotation Flag, Delete and Artifact, and List Numbering Details.
- Improved veraPDF integration and validation reporting, including an update to veraPDF 1.30.1 and showing previously hidden validation errors.
- Fixed tag and content ordering, retag cleanup, font pane reloads, and freezes in large document structure trees.

### User Interface

- Added Charcode column in Font Unicode Mapping view
- Fixed Custom Action dialog sizing in New and Edit mode
- Improved accessible colors
- Improved Fonts pane reload after document notifications

### Accessibility and Tagging

- Added Set Unicode for Font Charcode action
- Added support for expanding all selected tags
- Added Fix Invalid Elements action
- Added Set Annotation Flag action
- Added Delete and Artifact action in Struct Tree
- Added List Numbering Details widget in Tag Tree
- Fixed Find Annotation from Selection
- Fixed incorrect tag order after moving tags in Tag pane
- Fixed item ordering when moving content in Content pane
- Fixed Fix Content Marks action behavior
- Fixed empty tags left after retagging

### Actions and Workflows

- Registered Set Unicode for Font Charcode in action categorization and protection
- Registered Fix Invalid Elements in action categorization and protection
- Registered Set Annotation Flag in action UI, action categorization, and protection

### Validation and veraPDF

- Updated veraPDF to 1.30.2
- Fixed incorrect category in Validation Category View
- Fixed missing veraPDF errors in Desktop validation results

### Templates and Layout Recognition

- Added `font_update` support to templates for font actions

### Performance and Stability

- Improved deep Struct Tree loading with lazy fetch and batched MCID text scanning
- Added indexed child lookup to avoid expensive scans after tag moves
- Fixed Fonts pane reload after deleting font entries

## [3.0.0] - 2026-05-04

### Summary

This release focuses on a more practical application workspace, stronger external tagging workflows, and more flexible action execution directly in Document View.

- Improved usability and file handling in the Application Dashboard, including validation, preview, folder drag-and-drop, and clearer handling of opened files.
- Added and improved external actions for document tagging and tagging template creation, including Docling-based AutoTag and Create Layout Template workflows.
- Expanded custom action composition in Document View, including support for external actions, improved setup dialogs, and output handling into new tabs.

### User Interface

- Added validation preview in Application Dashboard
- Added support for dragging and dropping folders into a tab
- Added the Action pane and improved the action execution pane in Document View

### Accessibility and Tagging

- Added Add Child Tag action
- Added Move Tag action
- Added Move Up, Move Down, Level Up, Expand All, Collapse All, and Merge actions
- Added Alternate and Actual Text fields in Content pane
- Enabled artifact actions when tags are selected
- Added Split Content action
- Added Set List Numbering action
- Added automated fixes for validation errors
- Fixed link creation errors
- Fixed image tagging in Form XObject substructures

### Actions and Workflows

- Added Action pane in Document View
- Improved Action setup dialogs
- Added an option to save outputs into a new tab
- Added support for external actions in Document View
- Improved Custom Action editor ordering
- Added support for copying and pasting actions as JSON
- Improved batch progress and cancellation updates
- Added notifications for new action packages

### External Actions

- Improved Create Layout Template (Docling) and AutoTag (Docling) actions to support lists, complex tables, and element parenting
- Added a new external AutoTag (PDFix) action that uses layout templates and ensures backward compatibility by using the appropriate PDFix SDK version

### Validation and veraPDF

- Added Validation view in Application Dashboard
- Added veraPDF check highlighting in Preview
- Improved validation issue reporting
- Improved validation/layout integration
- Improved PAC and clause view switching

### Templates and Layout Recognition

- Improved Template pane loading
- Added template aliases
- Improved disabled template item behavior

### Performance and Stability

- Performance and stability improvements
- Threading and batch cancellation improvements

## [2.5.3] – 2025-12-18

### Summary

Minor update focused on improving application stability, user interface behavior, and license handling.

### User Interface

* Fixed an issue with moving files between tabs in the main application window
* Fixed loading and display of action titles

### License Management

* Fixed an issue with license deactivation when transferring the license to a new device

### General Updates

* Updated to **PDFix SDK 8.7.8**
* Performance, memory usage, and overall stability improvements across core operations


## [2.5.2] - 2025-10-16

### Summary
Minor update improving user experience and reliability in conversion workflows, navigation, and tag management.

### Manual Tagging
- Fixed issue with deleting tags after tagging
- Fixed crash occurring when *Tag As* action was canceled immediately after start

### User Interface
- Opening of external links from the Conversion pane to correctly launch in an external web browser
- Added **Previous / Next navigation** in Conversion View

### General Updates
- Updated to **PDFix SDK 8.7.6**
- Optimized performance, memory usage, and stability across all major operations.

## [2.5.1] - 2025-10-14

### Summary
Hotfix addressing issues with the cleanup and removal of empty tags after manual retagging.

### General
- Fixed an issue where empty tags were not correctly removed after retagging selected content in the Page View.

## [2.5.0] - 2025-10-09

### Summary
A major release focused on a **modernized user interface**, **enhanced document accessibility tools**, and **performance improvements** powered by **PDFix SDK 8.7.5**.

### User Interface  
**More intuitive and powerful workspace for document preview and actions.**

- **Main Application Window**
  - Introduced document preview directly in the main window.
  - Refactored *Run Action* dialog and *Activity* tab for better workflow visibility.
- **Document View**
  - Added new **Action Ribbon Toolbar** in the document window, including support for custom actions.  
  - Refactored output handling for conversion and validation reports (improved saving and organization).  
  - Added **tool buttons** for executing actions on selected content in document panes.  
  - Fixed issues in *Tag Destinations* view and *Create Link to Destination* functionality.  
- **Localization**
  - General translation fixes and UI improvements for multiple languages.

### Accessibility Actions  
**New tools to ensure PDF/UA and accessibility compliance.**

- Added **Document, Tags, or Content Language Detection** to identify missing or incorrect language attributes.  
- Added **Fix Link Tag** action — repairs invalid link tags and defines correct destinations and zoom settings.  
- Integrated new accessibility actions directly in the document window:
  - **Arlington PDF Model** — validates internal PDF syntax.
  - **Duplicate MCID Report** — detects duplicate marked content IDs.
  - **VeraPDF Validation** — generates full PDF/UA compliance reports.

### General Updates  
**Core improvements and SDK integration for faster, more reliable performance.**

- Integrated **PDFix SDK 8.7.5**  
- Optimized **performance, memory usage, and stability** across all major operations.


## [2.4.4] - 2025-09-05

### Accessibility 
- Added **Set Tag Language** action — enables support for tagging multi-language documents

### Template configuration
- Fixed handling of boolean variables in the layout template pane

### External Actions
- Added access to *External Actions* from the main application window toolbar
- Improved management of external actions and update notifications.

### User Interface
- Minor bug fixes and UX improvements
 
### General Updates
- Integrated **[PDFix SDK 8.7.4](https://github.com/pdfix/pdfix_sdk_builds/blob/main/changelog.md#874---2025-09-05)**
- Improved performance, memory usage, and stability

## [2.4.3] - 2025-08-11

### Accessibility 
- Added **Set Content Color** action — helps resolve issues with insufficient color contrast
- Added *Fix Page Orientation* action — unifies the page coordinate system with the page orientation and rotation
- Fixed an issue where text objects were split when tagging selected text

### External Actions
- Added **Amazon Textract* layout recognition action for layout template creation

### User Interface
- Various minor bug fixes
 
### General Updates
- **Integrated [PDFix SDK 8.7.3](https://github.com/pdfix/pdfix_sdk_builds/blob/main/changelog.md#873---2025-08-11)**
- Performance, memory, and stability improvements

## [2.4.2] - 2025-07-18

### Accessibility 
- Added action to remove annotation data (such as Contents)

### Template Configuration
- Add Table as Initial Element uses relative coordinates for cells

### External Actions
- Fixed import of actions with deprecated parameters
- Fixed issues with the execution of actions in the main application window
- Search box in the Add Action window
- Grayed files in the activity tab on Windows

### User Interface
- Consistent column widths in the new tabs in the main application window
 
### General Updates
- **Integrated [PDFix SDK 8.7.2](https://github.com/pdfix/pdfix_sdk_builds/blob/main/changelog.md#872---2025-07-18)**
- Performance, memory, and stability improvements

## [2.4.1] - 2025-07-10

### Accessibility 
- Fixed failures when moving structure elements in the Tag tree
- Document View actions hide unnecessary properties

### Template Configuration
- Message warning when opening old or incompatible templates

### External Actions
- Updated UX for external action management
 
### General Updates
- **Integrated [PDFix SDK 8.7.1](https://github.com/pdfix/pdfix_sdk_builds/blob/main/changelog.md#871---2025-07-10)**
- Various performance, memory, and stability improvements

## [2.4.0] - 2025-06-23

### Template Configuration
- Introduced object anchors for flexible object creation
- Added dynamic object bounding box definition
- Support for nested templates
- Added support for mathematical functions in templates
- Introduced Layout Recognition Debugger for advanced diagnostics

### External Actions
- Streamlined external action management
- Added support for new external actions:
  - Generate Alternate Text (Vision AI)
  - HTML to PDF conversion
  - Language detection
  - OCR using Tesseract
  - PDF Accessibility (OpenAI): Figure Alt Text, Table Summary, Formula MathML Associated Files
  - PDF Accessibility (Paddle): Auto-tagging, Formula MathML Associated Files
  - Arlington PDF syntax validation
 
### Validation
- Integrated veraPDF 1.29 for PDF/UA, WCAG validation

### User Interface
- Improved color contrast for better accessibility
- Added template JSON syntax validation, object match highlighting, and debugging tools
- Integrated in-app user notifications

### General Updates
- Native OS installers: Windows (MSI), macOS (DMG), Linux (RUN)
- **Integrated [PDFix SDK 8.7.0](https://github.com/pdfix/pdfix_sdk_builds/blob/main/changelog.md#870---2025-04-20)**
- Various performance and stability improvements

## [2.3.4] - 2025-04-15

### General Updates
- **Integrated [PDFix SDK 8.5.3](https://github.com/pdfix/pdfix_sdk_builds/blob/main/changelog.md#853---2025-04-15)**
  - Fixed tagging overlapping annotations over text content 
  - Fixed embedding TrueType fonts containing non-ansi characters

## [2.3.3] - 2025-03-28

### General Updates
- **Integrated [PDFix SDK 8.5.1](https://github.com/pdfix/pdfix_sdk_builds/blob/main/changelog.md#851---2025-03-28)**
  - Fixed duplicate MCID generated in content with nested content marks
  - Fixed missing tag name in BDC content mark in text content
  - Enhanced precision in matching annotations with text content

## [2.3.2] - 2025-03-14

### User Interface
- **Localization updates**

### Backend and Batch Processing
- **Fixed processing files with Unicode characters on Windows**

### General Updates
- **Integrated [PDFix SDK 8.5.0](https://github.com/pdfix/pdfix_sdk_builds/blob/main/changelog.md#850---2025-03-16)**
  - Added support for updating invalid document metadata
  - Fixed PDF-to-JSON export of text from structure elements, Base64 images, and annotations
  - Fixed updating of the document modified flag after running the set_pdf_version action
  - Fixed reloading of `PdePageMap` after a change in `PdfDocTemplate`
  - Fixed `xmp:ModifyDate` format in metadata
  - Fixed `remove_content_marks` action when removing invalid MCID in MCR structure elements
  - Fixed soft/hard hyphenation tagging
  - Fixed auto-tagging of text spans with annotations
  - Updated subscript/superscript detection in layout recognition
- **Performance and Stability improvements**    

## [2.3.1] - 2024-11-26

### User Interface
- Minor UI updates 
- Dutch language translation updates

### External Actions
- **Updated logging for executing external actions**
  - View log file for each processed file

### General Updates
- **Backend Enhancements**    

## [2.3.0] - 2024-11-22

### Accessibility and Tagging
- **New commands for remediation**
  - Clone Form XObjects (tagged and untagged)

### User Interface
- **New languages for user interface**
  - Čeština, Español, Suomi, Français, Magyar, Italiano, 한국어 (Hangul), 中文 (简体)
- **Shortcuts**
  - Updated custom shortcuts on macOS

### PDF/UA Validation
- **veraPDF** update to 1.27

### External Actions
- **Support for external docker-based actions**
  - [pdfix/verapdf-validation:v0.3.0](https://hub.docker.com/r/pdfix/verapdf-validation)
  - [pdfix/arlington-pdf-model:v0.3.0](https://hub.docker.com/r/pdfix/arlington-pdf-model)
  - [pdfix/html-to-pdf:0.4.2](https://hub.docker.com/r/pdfix/html-to-pdf)
  - [pdfix/alt-text-openai:v0.6.2](https://hub.docker.com/r/pdfix/alt-text-openai)
  - [pdfix/ocr-tesseract:v0.4.4](https://hub.docker.com/r/pdfix/ocr-tesseract)
  - [pdfix/alt-text-vision:v0.2.2](https://hub.docker.com/r/pdfix/alt-text-vision)
  - [pdfix/lang-detect:v0.4.3](https://hub.docker.com/r/pdfix/lang-detect)

### General Updates
- **Backend Enhancements**  
  - Integrated [PDFix SDK 8.4.0](https://github.com/pdfix/pdfix_sdk_builds/blob/main/changelog.md#840---2024-11-20)
  - Performance and stability improvements
  
## [2.2.2] - 2024-11-05

### User Interface
- **New languages for user interface**
  - Dutch, Dansk, Norsk, Svenska

### General Updates
- **Backend Enhancements**  
  - Integrated with [PDFix SDK 8.3.1](https://pdfix.net/support/changelog/)

## [2.2.1] - 2024-11-01

### General Updates
- **Backend Enhancements**  
- **Performance and Stability Improvements**

## [2.2.0] - 2024-10-30

### Accessibility and Tagging
- **Action Manager with Pipeline Runner Integration**  
  - Offers essential actions for editing PDF tags and metadata.  
  - Supports external actions using pre-configured Docker images for tasks such as OCR, HTML to PDF, Alt Text Generation, Language Detection, and more.  
  - Enables the creation of customizable action pipelines for batch processing on selected documents or entire folders.  

- **Template-Based Actions Configuration**  
  - Streamline workflows by targeting tags and other PDF objects with predefined templates.  

- **Tag Tool Enhancements**  
  - Simplifies the management of table headers and data cell associations.  
  - Provides options to select and modify tag properties and attributes.  

- **Professional Version Upgrades**  
  - Unlock advanced workflows with custom actions and pipeline capabilities.  

## User Interface
- **Tabbed Document Management**  
  - Enhances organization and navigation across multiple documents for a more efficient workflow.  

- **New Toolbars**  
  - Provides quick access to frequently used features, streamlining the user experience.  

## General Updates
- **Backend Enhancements**  
  - Integrated with PDFix SDK 8.3 for improved functionality.  
  - Updated to VeraPDF v1.25 for enhanced PDF/UA compliance.  

- **Performance and Stability Improvements**  
  - Continuous enhancements for a more stable and responsive experience. 

## [2.1.0] - 2024-08-07

### Accessibility and Tagging
- New Quick Fix action for automated fixing of common minor accessibility issues
- Updated Delete Tags action with option to mode children to parent structure element
- Fixed generating duplicate MCID and invalid unicode encoding table
- Fixed lost content when flattening Form XObjects

### User Interface
- Validation results related to specific pages organized by pages
- Fixed Quick Access Tag As... buttons hidden after the update

### General
- Native support for macOS Silicon chip architecture


## [2.0.1] - 2024-05-11

### Accessibility and Tagging
- Updated default tagset for PDF version 1.3 and lower
- Batch commands management update

### User Interface
- Fixed Quick Access Tag As... buttons hidden after the update

### General
- Fixed MacOS installer does start or check for update


## [2.0.0] - 2024-05-02

### Accessibility, Tagging, and Validation
- Command categories
- New remediation commands for document and batch {see PDFix SDK change log}
- Save validation report to HTML
- New customizable Make Accessible and Autofix commands

### User Interface
- Quick access toolbar
- Unified command dialogs
- Font pane sorting
- Shortcut search in Preferences

### General
- New MacOS native support for ARM architecture (M1, M2, M3 chip)
- [Integrated PDFix SDK 8.0.1](https://github.com/pdfix/pdfix_sdk_builds/blob/main/changelog.md#801---2024-05-03)
- Performance and stability improvements

## [1.5.3] - 2024-03-13

### Accessibility, Tagging, and Validation
- Fixed unwanted table columns created with text filling when tagging as table
- Duplicated MCID created when tagging

### General
- [Integrated PDFix SDK 7.3.3](https://github.com/pdfix/pdfix_sdk_builds/blob/main/changelog.md#733---2024-03-13)
- Performance and stability improvements

## [1.5.2] - 2024-02-27

### Accessibility, Tagging, and Validation
- Enhanced character Unicode mapping

### HTML Conversion
- Append custom HTML to the end of the body

### General
- [Integrated PDFix SDK 7.3.2](https://github.com/pdfix/pdfix_sdk_builds/blob/main/changelog.md#732---2024-02-27)
- Performance and stability improvements

## [1.5.1] - 2024-02-16

### Accessibility, Tagging, and Validation
- Changed Copy/Paste Tag shortcuts
- Save Validation results

### HTML Conversion
- Conversion to HTML from PDF Tags (derivation) encoding fix

### General
- [Integrated PDFix SDK 7.3.1](https://github.com/pdfix/pdfix_sdk_builds/blob/main/changelog.md#731---2024-02-16)
- Performance and stability improvements

## [1.5.0] - 2024-01-23

### Accessibility, Tagging, and Validation
- Customizable quick Tag As actions
- Added validation profiles for ISO-32000, PDF/UA, WCAG, and more
- Table tool keyboard navigation and moving with CTRL/SHIFT
- Cut and Paste Tag as sibling or child

### Batch Commands
- Added Set PDF/UA Standard command update
- Added Import/Clone command 
- Enabled command editing before run
- Display progress when running batch commands
- Memory consumption improvements in batch

### General
- Mouse wheel page zoom control
- Watermark warning message before saving in the Lite version
- PDFix SDK updated to 7.3.0
- VeraPDF updated to 1.25.0
- Performance and stability improvements

## [1.4.0] - 2023-09-22

### Accessibility & Tagging
- Add/Edit Table Summary
- Delete Tags Comand simplified

### HTML Conversion
- Integrated HTML preview

### General
- Batch processing performance update
- Rotate Pages
- Document permissions check
- Integrated PDFix SDK 7.1.0
- Performance and stability improvements

## [1.3.1] - 2023-07-28

### Batch Commands
- Delete Tags, Set Contents 
- Fix placement for Notes

### General
- Performance and stability improvements

## [1.3.0] - 2023-06-28

### Accessibility and Tagging
- Enhanced Table Editor

### Batch Commands
- Fix Whitespaces
- Remove Tag Properties
- Set Structure Element Attribute

### General
- PDF structure editor with Arlington grammar
- Performance and stability improvements
