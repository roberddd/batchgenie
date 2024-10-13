---
tags:
  - Release history
hide:
  - navigation
  - toc
---
Here, you can find a list of all updates, enhancements, and bug fixes made to BatchGenie over time. Date Format: YYYY-MM-DD.

### Versions

<div class="changelog" markdown>

#### 1.1.2

  > Date: 2024.10.13

- **Improved functionality**:
    - `Exporting `: When exporting via the Asset Browser, you now have the option to export selected assets as a single combined blend file, in addition to saving them as individual files.
- **Bugfix**:
    - **CRITICAL**: `Add Tags`: A previous update caused all 'Smart Tags' to stop working. This issue has now been resolved, restoring full functionality to the tagging system.

---

#### 1.1.1

  > Date: 2024.10.13

- **Improved functionality**:
    - `Exporting `: When exporting via the Asset Browser, you can now add a suffix to handle duplicate asset names. For instance, if you're exporting two assets both named "Cube," you can choose how they are renamed, such as "Cube.blend" and "Cube (2).blend".
- **Bugfix**:
    - `Exporting`: Fixed an issue where exporting local Assets from your current file via the Asset Browser, while not in the 'Current File' library, resulted in empty .blend files. This has now been resolved.

---

#### 1.1.0

  > Date: 2024.10.12

- **Bugfix**:
    - `Rendering`: Fixed an issue where rendering for certain collections would complete, but the cleanup of temporary files failed due to specific material node-groups. As a result, BatchGenie was unable to set the newly rendered image as the Asset thumbnail. This has now been resolved.
- **UI**:
    - `Exporting`: A progress bar is now displayed when exporting, with plans to implement it in other areas soon.

---

#### 1.0.9

  > Date: 2024.10.10

- **New functionality**:
    - `Importing`: Batch import of blend files is now available. Import Objects, Collections and Materials. [More info](import.md#import-blend-files)
- **Improved functionality**:
    - `Rendering Assets`: The chosen 'Lighting Setup' will now be saved, so the next time you start Blender, it will remember your setting.
- **UI**:
    - Redesigned Add-on `Preferences` with a new tabbed layout, replacing the previous single-page "wall of text" format for better organization and usability.

---

#### 1.0.8

  > Date: 2024.10.07

- **New functionality**:
    - `Exporting`: Now integrated into the Asset Browser. More settings added; customize the export name & pack texture option. [More info](export.md)
    - New utility `Pack Textures`: Inside the Asset Browser, you can now select Assets and pack the textures for these Assets, ensuring that your Assets maintain their appearance without relying on external texture files. [More info](utilities.md#pack-textures)
- **Bugfix**:
    - `Exporting`: The `Keep Outliner Hierarchy` setting now correctly exports objects that are directly in the root Scene Collection.
    - Utility `Load previews from disk`: Sometimes when selecting the folder, the current blend file was selected in the file browser, causing the selected file path to include the .blend file, which resulted in no previews being found. This has now been resolved.
- **UI**:
    - Minor UI and layout adjustments.

---

#### 1.0.7

  > Date: 2024.10.05

- **New / Improved functionality**:
    - `Exporting `: The functionality has been expanded to support exporting collections and materials. New options are now available to customize the export process. [More info](export.md)

---

#### 1.0.6

  > Date: 2024.10.04

- **New functionality**:
    - New `Export objects`: Basic exporting functionality added. In the near future, the export functionality will be expanded and will also be available in the Asset Browser for easy exporting of your Assets in various formats. [More info](export.md)
- **Improved functionality**:
    - Utilities: Enhanced parallel processing speed. When working with external blend files, BatchGenie utilizes multiple Blender processes in the background for quicker performance. Now with even greater speed, achieving up to a 0.5-second improvement per external blend file opened.
- **Bugfix**:
    - `Rendering Assets`: A potential issue that could cause minor problems with cleaning temporary files after rendering has now been resolved.

---

#### 1.0.5

  > Date: 2024.10.03

- **Bugfix**:
    - **CRITICAL**: `Rendering Assets`: Rendering Assets via the Asset Browser that are already present in your open scene may result in those objects being deleted from the scene. This issue has now been fixed, along with improvements to how temporary data is handled internally.
    - Utility `Replace Shader Nodes` / Import Textures > setting `Replace Principled BSDF`: Geometry nodes are now filtered out, displaying only Shader Editor nodes in the dropdown.

---

#### 1.0.4

  > Date: 2024.10.01

- **Improved functionality**:
    - Utility `Load previews from disk`: Now supports more image formats.
- **Bugfix**:
    - **CRITICAL**: `Rendering Assets`: Issue with rendering objects via the Asset Browser caused in 1.0.3 update. Now fixed.

---

#### 1.0.3

  > Date: 2024.10.01

- **New functionality**:
    - New Utility `Load previews from disk`: Load custom Asset Preview images from a specified directory. [More info](utilities.md#load-previews-from-disk)
- **Bugfix**:
    - **CRITICAL**: Importing Textures: Importing metallic textures had unfortunately broken in one of the updates leading to 1.0.0. This has now been fixed.

---

#### 1.0.2

  > Date: 2024.09.27

- **New functionality**:
    - Utility `Add Asset Tag`: New Smart Tag: 'Material Type'. Tags the material with its type: "Texture-based" or "Procedural", with an option to include node counts for both types. Example: "Procedural (56 nodes)". [More info](utilities.md)
    - `Render Asset Previews`:  'Add Incremental Filename Suffix' option: When saving Asset previews externally, this feature automatically appends an incrementing number to the end of filenames, ensuring each version is saved without overwriting previous files. This allows you to quickly iterate renders with various settings. For example, if your object is named "Suzanne", rendered images will be saved as "Suzanne[1].png", "Suzanne[2].png", etc. [More info](render_asset_previews.md#render-settings)
- **UI**:
    - Improved UI & tooltips for the previously added 'Filtering' functions for some utilities.
    - Improved the layout & content of the 'info' popup that is available in many places.
    - Added info button to the 'render settings' that displays useful information.
- **Bugfix**:
    - Utility `Replace Shader Nodes`: The option 'Only materials imported by BatchGenie' did not work this utility but is now fixed.

---

#### 1.0.1

  > Date: 2024.09.25

- **New functionality**:
    - Utilities: `Change Node Attributes`, `Change Material Settings`, & `Replace Shader Nodes`: New keyword filtering function to filter materials by their names to include or exclude them from the batch process.
- **Improved functionality**:
    - Utilities: `Change Node Attributes`, `Change Material Settings`, & `Replace Shader Nodes`: 'Selection' dropdown has new options: 'Materials marked as Assets' & 'Materials NOT marked as Assets' to help target specific materials.
    - Utility: `Batch Rename`: the 'Set Mesh names same as Object names' setting now has a 'Selection' dropdown, which helps you target specific objects such as selected objects, etc., and not just all objects in your file.
- **UI**:
    - Minor layout adjustments and a few typos fixed
- **Misc**:
    - 'Only materials imported by BatchGenie' setting is no longer on by default.

---

#### 1.0.0

  > Date: 2024.09.21. Compatibility: Blender 4.2 LTS +

  - First public release.

</div> <!-- /Changelog -->