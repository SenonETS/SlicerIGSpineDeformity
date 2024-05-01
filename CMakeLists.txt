cmake_minimum_required(VERSION 3.16.3...3.19.7 FATAL_ERROR)

project(SlicerIGSpineDeformity)

#-----------------------------------------------------------------------------
# Extension meta-information
set(EXTENSION_HOMEPAGE "https://github.com/SenonETS/SlicerIGSpineDeformity#readme")
set(EXTENSION_CATEGORY "IGT")
set(EXTENSION_CONTRIBUTORS "Sen Li (École de technologie supérieure)")
set(EXTENSION_DESCRIPTION "This Module is designed for spine deformity analysis using freehand 3D ultrasound imaging, and the first module Lamina Landmark Labeling help find the Spinal Cord curve in 3D, which can be projected to three anatomical planes, e.g., for Scoliosis analysis using the Cobb angle when projected to the front back view.")
set(EXTENSION_ICONURL "https://raw.githubusercontent.com/SenonETS/SlicerIGSpineDeformity/main/SlicerIGSpineDeformity_Icon_128x128.png")
set(EXTENSION_SCREENSHOTURLS "https://raw.githubusercontent.com/SenonETS/SlicerIGSpineDeformity/main/sl_01__LaminaLandmark_Labeling/SL_ScreenShot.PNG")
set(EXTENSION_DEPENDS "NA") # Specified as a list or "NA" if no dependencies

#-----------------------------------------------------------------------------
# Extension dependencies
find_package(Slicer REQUIRED)
include(${Slicer_USE_FILE})

#-----------------------------------------------------------------------------
# Extension modules
add_subdirectory(sl_01__LaminaLandmark_Labeling)
## NEXT_MODULE

#-----------------------------------------------------------------------------
include(${Slicer_EXTENSION_GENERATE_CONFIG})
include(${Slicer_EXTENSION_CPACK})
