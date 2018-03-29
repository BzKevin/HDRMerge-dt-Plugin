# HDRMerge-dt-Plugin 
HDRMerge plugin for darktable

This plugin adds the module "HDRMerge" to darktable's lighttable view.

## Dependencies: 
OS: Windows (tested), Linux (not verified), MacOS (not verified).
HDRMerge 4.5 or greater.

## How to use: 
Require this file from your luarc file, as with any other dt plug-in.
On initial run setup HDRMerge's install path via the settings > lua options dialog. Restart may be required.
Select a group of photos you desire to merge and press HDRMerge.

## Options: 
Bits Per Sample - Bit depth of the final image.
Preview Size - Preview size of the built-in preview.
Batch - Allows user to select multiple groups and HDRMerge will auto-group them based on time seperation "gap".
Gap - Time seperation between groupings when running in batch mode.
Style - Style to be applied when image is auto-imported (Auto-import only supported in non-batch mode).
Copy Tags - Enable to copy tags from first file in selection.
Additional Tags - Additional tags to be added, works with or without Copy Tags enabled.

## Versions:
Version 0.1 - Implemented via "Selected Images"
Version 0.2 - Implemented as it's own module - windows only
Version 0.3 - Improved cross-platform compatibility, improved performance ( switched from io.popen() to dt.control.execute() )
Version 1.0 - Added:
			Copy Tags Option
			Additional Tags Option
			User Defined Default Style
			Progress Bar
	1.0.1 - Added check for at least 2 images selected
		Fixed issue with status bar not disappearing when HDRmerge not installed or not enough images selected
	1.0.2 - Changes for grabbing executable path and setting preference (to imporve cross-platform support)
		Changes to building the run_cmd (to improve cross-platform support)
