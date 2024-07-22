PROJECT(MixingOpenGLandVTK)
CMAKE_MINIMUM_REQUIRED(VERSION 2.8)

FIND_PACKAGE(VTK REQUIRED)
INCLUDE(${VTK_USE_FILE})

ADD_EXECUTABLE(RenderInExistingContext RenderInExistingContext.cxx)
TARGET_LINK_LIBRARIES(RenderInExistingContext vtkCommon vtkGraphics vtkIO vtkFiltering vtkRendering vtkVolumeRendering)
