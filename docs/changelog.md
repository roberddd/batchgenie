---
tags:
  - Release history
hide:
  - navigation
  - toc
---
Here, you can find a list of all updates, enhancements, and bug fixes made to BatchGenie over time. Date Format: YYYY-MM-DD.

### Versions

#### 1.0.4

  > Date: 2024.10.01

- **Improved functionality**:
    - Utility `Load previews from disk`: Now supports more image formats.

- **Bugfix**:
    - **CRITICAL**: Rendering objects: Issue with rendering objects via the Asset Browser caused in 1.0.3 update. Now fixed.



#### 1.0.3

  > Date: 2024.10.01

- **New functionality**:
    - New Utility `Load previews from disk`: Load custom Asset Preview images from a specified directory. [More info](utilities.md#load-previews-from-disk)

- **Bugfix**:
    - **CRITICAL**: Importing Textures: Importing metallic textures had unfortunately broken in one of the updates leading to 1.0.0. This has now been fixed.


#### 1.0.2

  > Date: 2024.09.27

- **New functionality**:
    - Utility `Add Asset Tag`: New Smart Tag: 'Material Type'. Tags the material with its type: "Texture-based" or "Procedural", with an option to include node counts for both types. Example: "Procedural (56 nodes)". [More info](utilities.md#Asset-tags-add-material-type)
    - `Render Asset Previews`:  'Add Incremental Filename Suffix' option: When saving asset previews externally, this feature automatically appends an incrementing number to the end of filenames, ensuring each version is saved without overwriting previous files. This allows you to quickly iterate renders with various settings. For example, if your object is named "Suzanne", rendered images will be saved as "Suzanne[1].png", "Suzanne[2].png", etc. [More info](render_asset_previews.md#render-settings)

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
    - Minor layout adjustments.
    - A few typos fixed.

- **Misc**: 'Only materials imported by BatchGenie' setting is no longer on by default.

---

#### 1.0.0

  > Date: 2024.09.21. Compatibility: Blender 4.2 LTS +

  - First public release.
