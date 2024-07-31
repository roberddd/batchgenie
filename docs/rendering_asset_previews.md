---
tags:
  - HDRi
---
When it comes to rendering Asset Preview images, you have two distinct options. You can either utilize Batch Rendering through the BatchGenie panel, or selectively choose Assets from the Asset Browser for which you wish to render previews for. BatchGenie supports rendering previews for materials, objects & collections.


## Batch Rendering

![Batch Render](images/generate_asset_previews_objects.png){ .img-box align=right }

1. Open the BatchGenie panel.
2. Go to the `Generate Asset Previews` section in the panel.
3. Choose the Asset type you want to render previews for and select the appropriate filters to target the Assets that need previews.
4. Configure the scene and render settings as needed.
5. Click `Batch Render`, and BatchGenie will render all Assets that fit your selection filter.


<div style="clear:both"></div>


## Rendering via Asset Browser

1. Open the Asset Browser in Blender.
2. Select the Assets you want to render.
3. Locate the BatchGenie menu.
4. Configure the scene and render settings as needed.
5. Click on `Render selected Assets` and BatchGenie will render all selected Assets.



![Asset Browser Render](images/generate_asset_previews-render_from_asset_browser.gif){ .img-box }


<div style="clear:both"></div>


## Settings

You can access the settings through both the BatchGenie panel and the BatchGenie menu in the Asset Browser.


#### Asset Selection

=== "Objects"
    ![Asset Preview Panel](images/generate_asset_previews_objects.png){ .img-box align=left }

    - **Selection**: Allows you to specify which objects to include in the rendering process based on predefined criteria. Options listed below:
        - **Selected Objects**: Choose the currently selected object(s) in your scene. When using this option, you have the option to mark the objects as Assets:
        - **Objects marked as Assets**: Objects in the your file that are marked as Assets.


    <div style="clear:both"></div>

    - **Refine**: Helps you to refine the selection made with the 'Selection' function by applying additional criteria.
        - **Missing Previews**: Selects objects that are missing Asset Previews.
        - **Low-Quality Previews**: Selects objects with existing Asset Previews below 256px in resolution.
        - **Low-Quality & Missing Previews**: Selects objects with existing Asset Previews below 256px in resolution, as well as objects without Asset Previews.
        - **No Filter (all objects)**: Selects all objects that match the previous selection without any further filtering.

    - **Mark as Asset**: Marks the objects as Assets. This option is shown depending on the 'Selection' option. This option can only be disabled if you are saving previews externally (see [Render Settings](#render-settings)).


=== "Collections"
    ![Asset Preview Panel](images/generate_asset_previews_collections.png){ .img-box align=left }

    - **Selection**: Allows you to specify which collections to include in the rendering process based on predefined criteria. Options listed below:
        - **Selected Collection**: Choose the currently selected collection in your scene. When using this option, you have the option to mark the collection as an Asset:
        - **Collections marked as Assets**: Objects in the your file that are marked as Assets.

    <div style="clear:both"></div>

    - **Refine**: Helps you to refine the selection made with the 'Selection' function by applying additional criteria.
        - **Missing Previews**: Selects collections that are missing Asset Previews.
        - **Low-Quality Previews**: Selects collections with existing Asset Previews below 256px in resolution.
        - **Low-Quality & Missing Previews**: Selects collections with existing Asset Previews below 256px in resolution, as well as collections without Asset Previews.
        - **No Filter (all objects)**: Selects all collections that match the previous selection without any further filtering.

    - **Mark as Asset**: Marks the collections as Assets. This option is shown depending on the 'Selection' option. This option can only be disabled if you are saving previews externally (see [Render Settings](#render-settings)).

=== "Materials"
    ![Asset Preview Panel](images/generate_asset_previews_materials.png){ .img-box align=left }

    - **Selection**:  Allows you to specify which materials to include in the rendering process based on predefined criteria. Options listed below:
        - **Materials on Selected Objects**: All materials assigned to the the currently selected object(s) in your scene. When using this option, you have the option to mark the materials as Assets.
        - **Materials marked as Assets**: Materials in your file that are marked as Assets.
        - **All materials**: All materials in your file regardless if they are marked as Assets or not. When using this option, you have the option to mark the materials as Assets.

    <div style="clear:right"></div>

    - **Refine**: Helps you to refine the selection made with the 'Selection' function by applying additional criteria.
        - **Missing Previews**: Selects materials that are missing Asset Previews.
        - **Low-Quality Previews**: Selects materials with existing Asset Previews below 256px in resolution.
        - **Low-Quality & Missing Previews**: Selects materials with existing Asset Previews below 256px in resolution, as well as materials without Asset Previews.
        - **No Filter (all materials)**: Selects all materials that match the previous selection without any further filtering.

    - **Only materials imported by BatchGenie**:  When enabled, this option ensures that the batch operation only affect materials imported by BatchGenie. Disabling it applies changes to all materials in your file, regardless of their origin.
    - **Mark as Asset**: Marks the materials as Assets. This option is shown depending on the 'Selection' option. This option can only be disabled if you are saving previews externally (see [Render Settings](#render-settings)).

---


#### Scene Settings

![Scene Settings](images/generate_asset_previews_scene_settings.png){ .img-box align=left }

- **Light Preset**: Choose from a selection of different lighting presets to enhance your renders. Options include various sky setups as well as Blender's built-in HDRIs. There is also a 'Custom World' option that utilizes your scene's current 'World' for lighting, allowing you to use your own HDR images.

    ??? abstract "Light Presets Example"
        ![Light Presets](images/generate_asset_previews-lighting_presets.png){ .img-box .on-glb }

- **Studio Preset**: Allows you to add a studio backdrop as a background if desired.

    ??? info2 "Studio Settings"

        ![Studio Settings](images/generate_asset_previews_studio_settings.png){ .img-box }

        Settings to customize the backdrop:

        - **Material**: Use either the default material, with adjustable color and roughness, or choose your own material.
        - **Transparent Backdrop**: *(Cycles Only)* Makes the studio backdrop see-through while remaining visible in reflections and bouncing back light to the objects.
        - **Backdrop passes light**: *(Cycles Only)* Enables the backdrop to allow light to pass through it, preventing it from blocking light from world lights.

- **Transparent Background**: Enables a transparent background in rendered images

<div style="clear:both"></div>

- **Light Strength**: Adjusts the strength of the world background.

- **Rotation**:
    - **Sun Rotation**: Adjusts the horizontal angle of the sunlight in your scene or rotates the HDRI background for lighting. This changes the direction from which light illuminates objects.
    - **Object Rotation**: Adjusts the rotation of the object.
    - **Camera Rotation**: Adjusts the rotation of the camera. Useful when you want to keep the lights & shadows in their current position but want to change the framing.

    !!! info2 "Tip"
        *You can also use the icon buttons to the left & right of the slider to adjust them -/+ 45 degree increments.*

??? info2 "Camera Settings"
    ![Camera Settings](images/generate_asset_previews_camera_settings.png){ .img-box align=left }

    - **Vertical Angle**: Adjusts the vertical angle of the camera, moving it up or down to change the perspective from which the scene is viewed, either looking up or down.

        ??? abstract "Vertical Angle Example"
            ![Camera Angle Example](images/generate_asset_previews-camera_angle_example.png){ .img-box }

    - **Zoom**: Adjust the camera distance from the object. Zoom in for a close-up view or zoom out to add space around your object.
    - **Focal Length**: Adjusts the focal length of the camera, affecting the field of view and perspective. A shorter focal length increases the field of view, creating a wide-angle effect, while a longer focal length decreases the field of view, producing a zoomed-in effect.

    <div style="clear:both"></div>

    - **Exposure**:  Adjusts the overall brightness of your scene by controlling the amount of light that reaches the camera, effectively brightening or darkening the rendered image.

        ??? abstract "Exposure Example"
            ![Exposure Example](images/generate_asset_previews-exposure_example.png){ .img-box }

    - **Override camera orientation with**: Lets you use a custom camera angle. Choose between:

        - **View**: Set the render camera to match the current 3D view's perspective, ensuring the render viewpoint aligns with the 3D viewport
        - **Active Camera**: Set the render camera to the position and orientation of the active camera, ensuring the render viewpoint matches the current active camera's view.

        When using override you also have the **Autoframe** option available that automatically adjusts the camera to frame the selected object perfectly, ensuring that it fits within the view without any clipping. Disable this option for manual framing of your Asset, such as for close-up shots.


- **Material Preview Object**:

    These settings are used when rendering material Assets.

    - **Preview Object**: Select the model type used to display the material preview. Choose from options Sphere, Suzanne, Cylinder, or Custom. The Custom option allows you to use the currently selected object in your scene as the preview model.
    - **Clear current materials**: When rendering previews using the 'Custom Object' option, enable this setting to show only the previewed material on the object. Disable to retain existing materials on the object, assigning the preview material to slot 1. Useful for objects with multiple materials.
    - **Subdiv**: The number of subdivisions to apply to the model.
    - **Adaptive Subdiv**: *(Cycles Only)* Dynamically adjusts the level of detail for subdivided surfaces based on the camera distance, optimizing render times while maintaining high-quality details where needed. Useful for materials with displacement.

---


#### Render Settings

![Render Save Location](images/generate_asset_previews_render_settings.png){ .img-box align=left }

Here, you'll find settings for aspect ratio, resolution, and other Blender default render settings you're likely already familiar with.

!!! info2 "Asset Preview Resolution"
    When rendering images to use as previews for the Assets themselves, note that previews saved inside the Asset are limited to 256x256 pixels. With that said, the recommended render resolution is 512x512, which improves overall sharpness even if saved at a lower resolution afterward. This offers an improvement over Blender's default Asset Preview resolution of 128x128 pixels.

<div style="clear:both"></div>

- **Output**: Determines where your rendered images are saved. You can choose between:
    - **Save in Asset**: to save images within the Blender file.
    - **Save in Asset & Save Externally**: to save both within the file and as separate external files.
    - **Save Only External**: to save images only as external files.


## FAQ

- **Can I add custom Light Presets?**
    - Yes! The list can be expanded by directly adding your own HDRIs to blender via `Preferences > Lights > HDRI's` which makes them available in this list.
- **How do I adjust the Light Paths settings for renders?**
    - These settings from your current scene will be used. To adjust them, go to `Render > Light Paths` in the Properties panel and make your desired changes there.
- **I'm having issues with the adaptive subdivision being slow in Cycles. What can I do?**
    - Adjust your `Subdivision Dicing Rate` in your current scene, as the render will use those settings. First, ensure that the "Experimental" Feature Set is enabled under `Render > Feature Set` in the Properties panel. Then, go to `Render > Subdivision` and increase the `Dicing Rate Render` value.


## More adjustments in Preferences {#more-settings data-search-exclude}

See the add-on [Preferences](preferences.md) for more settings related to rendering.