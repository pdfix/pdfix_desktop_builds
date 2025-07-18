# PDFix Desktop changelog

## New Features & Updates

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
