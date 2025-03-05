The BlazorBootstrap grid does not work
https://github.com/vikramlearning/blazorbootstrap/issues/887

# How this project was created

VisualStudio 2022 (17.12.1).

Create a new blazor project.

Install package `Blazor.Bootstrap` in the server side project.

There is no file `wwwroot\index.html` therefore it is impossible to follow the instructions at https://docs.blazorbootstrap.com/getting-started/blazor-webassembly-net-8.
Instead add the CSS and scripts to `Components\App.razor` seems to work and add `builder.Services.AddBlazorBootstrap()` to `Program.cs`.

There is no folder `wwwroot\css\bootstrap`.

Add `@using BlazorBootstrap;` to `_Imports.razor`.

There isn't a `MainLayout.razor`

# Witness the grid not working

In the server side project add a new _Razor component_ `Components/Pages/GridExample.razor`.

In the client side project edit `Pages/Home.razor` to add a link to the new page which is at `/GridExample`.

Copy the example from https://demos.blazorbootstrap.com/grid.

Run the project and navigate to the grid example page. The page appears but without the grid. It then disappears and says _Not found_.
