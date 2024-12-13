# Localization of Syncfusion WPF Controls using .resx files        

This repository contains the default resource files (.resx) of Syncfusion WPF libraries. You can use this resource files to localize the strings for any selected language. 

## Localization of Syncfusion WPF Controls

Localization is the process of translating the application resources into different language for the specific cultures. You can localize the syncfusion WPF controls by adding resource file for each language.

### Changing application culture

When you are changing the application culture, then you can localize the application based on application culture by creating .resx file.

```
public MainWindow()
{
    System.Threading.Thread.CurrentThread.CurrentUICulture = new System.Globalization.CultureInfo("de-DE");
    InitializeComponent();
}
```

### Creating .resx files

You can create .resx files for any language by following below steps,

1) Right click your project and add new folder named `Resources`. 

2) Add default resource files of libraries you are using into `Resources` folder and ensure `AccessModifier` specfied as `Public`. 

> Consider you are using `SfDataGrid` and `Ribbon` in your application. Then you need to copy and include `Syncfusion.SfGrid.WPF.resx` (since `SfDataGrid` present in `Syncfusion.SfGrid.WPF` library) and `Syncfusion.Tools.Wpf.resx` (since `Ribbon` present in `Syncfusion.Tools.WPF` library) files in your application under `Resources` folder. So, now you can know the key names and values of default stings used in `Syncfusion.Tools.WPF.dll` and `Syncfusion.SfGrid.WPF.dll` libraries.    

![WPF DataGrid Localization](https://help.syncfusion.com/wpf/localization-images/wpf-default-resx-file.png)

3) Now, right click `Resources` folder and select `Add` and then `NewItem`. In the In `Add New Item` wizard, select the Resource File option and name the filename as `Syncfusion.SfGrid.WPF.<culture name>.resx`. For example, you have to give name as `Syncfusion.SfGrid.WPF.de.resx` for `German` culture. In the same way, add new resource files for other libraries used in your application.

![WPF Control Localization](https://help.syncfusion.com/wpf/localization-images/wpf-adding-resource-file.png)

4) Now, select `Add` and add resource file for german culture in `Resources` folder and set `AccessModifier` property to `No code generation`.  

![WPF Control Localization using .resx file](https://help.syncfusion.com/wpf/localization-images/wpf-resx-file-to-localize.png)


5) Now, you can copy the key names from default resource files and assign value based on the culture the resource files targets. 

![](https://help.syncfusion.com/wpf/localization-images/wpf-localized-resx-file.png)

> Download demo from [GitHub](https://github.com/SyncfusionExamples/wpf-datagrid-localization)

## Editing default culture strings

You can change default string of any control by adding the default .resx files ([from Github](https://github.com/syncfusion/wpf-controls-localization-resx-files)) to `Resources` folder of your application.  Syncfusion WPF controls reads the default string from the .resx files of application if its added.   