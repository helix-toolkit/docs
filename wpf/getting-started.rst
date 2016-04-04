===============
Getting started
===============

.. note:: This section is under construction. Please contribute!

- Adding the "HelixToolkit.Wpf" NuGet package
- Adding a `HelixViewport3D` control
- Adding content

Adding the "HelixToolkit.Wpf" NuGet package
----------

You can add a NuGet package by right clicking on your project, and then selecting `manage NuGet packages ...`. There you can search for and add `HelixToolkit.Wpf`.

Adding the toolkit to your xaml
----------

in the `Window` node of your xaml you have to add a new key to reference the toolkit. It should look like `xmlns:HelixToolkit="clr-namespace:HelixToolkit.Wpf;assembly=HelixToolkit.Wpf"`. This makes your window look something like: 

::

  <Window x:Class="YourNamespace.MainWindow"
          xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
          xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
          xmlns:d="http://schemas.microsoft.com/expression/blend/2008"
          xmlns:mc="http://schemas.openxmlformats.org/markup-compatibility/2006"
          xmlns:HelixToolkit="clr-namespace:HelixToolkit.Wpf;assembly=HelixToolkit.Wpf" 
          xmlns:local="clr-namespace:YourNamespace"
          mc:Ignorable="d"
          Title="MainWindow" Height="350" Width="525">

Adding a viewport control
---------

Now you can add the helix viewport control like you would add a regular 3D control. Your `Grid` should now contain: 

::

  <HelixToolkit:HelixViewport3D ZoomExtentsWhenLoaded="True">
      <!-- Remember to add light to the scene -->
      <HelixToolkit:SunLight/>
      <ModelVisual3D>
          <ModelVisual3D.Content>
              <GeometryModel3D>
                  <GeometryModel3D.Geometry>
                      <MeshGeometry3D x:Name="meshMain"
                          Positions="0 0 0  1 0 0  0 1 0  1 1 0  0 0 1  1 0 1  0 1 1  1 1 1"
                          TriangleIndices="2 3 1  2 1 0  7 1 3  7 5 1  6 5 7  6 4 5  6 2 0  2 0 4  2 7 3  2 6 7  0 1 5  0 5 4">
                      </MeshGeometry3D>
                  </GeometryModel3D.Geometry>
                  <GeometryModel3D.Material>
                      <DiffuseMaterial x:Name="matDiffuseMain">
                          <DiffuseMaterial.Brush>
                              <SolidColorBrush Color="Gray"/>
                          </DiffuseMaterial.Brush>
                      </DiffuseMaterial>
                  </GeometryModel3D.Material>
              </GeometryModel3D>
          </ModelVisual3D.Content>
      </ModelVisual3D>
      <HelixToolkit:GridLinesVisual3D Width="8" Length="8" MinorDistance="1" MajorDistance="1" Thickness="0.01"/>
  </HelixToolkit:HelixViewport3D>

You can also see simple examples on the [repository](https://github.com/helix-toolkit/helix-toolkit/tree/master/Source/Examples) of helix-toolkit
