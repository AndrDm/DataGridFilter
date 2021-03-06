<!--
Edited
https://dillinger.io/
-->

# WPF Filterable Datagrid, multi language
![datagrid image demo](datagridFilter.png)

## How to use
 - Include the **FilterDataGrid** folder in your project   

 - Add **FilterDataGrid.xaml** to App.xaml as MergedDictionaries   
```
    <Application.Resources>
        <ResourceDictionary>
            <ResourceDictionary.MergedDictionaries>
	    	<ResourceDictionary Source="FilterDataGrid/FilterDataGrid.xaml" />
		...
```  
   
 - Add **FilterDatagrid** into your xaml :   
 
      - **Namespace**      
		`xmlns:control="clr-namespace:FilterDataGrid"`
	  - **Control**   
		`<control:FilterDataGrid ...`   
		- Available properties
		  - **ShowStatusBar** : *displays the status bar* (bool)
		  - **ShowElapsedTime** : *displays the elapsed time of filtering in status bar* (bool)
		  - **DateFormatString** : *date display format* (string)   
		> if you add custom columns, you must set the **AutoGenerateColumns** property to "False"  
		
	  - **Custom colum**   
		```
		<control:FilterDataGrid.Columns>   
		    <control:DataGridTextColumn IsColumnFiltered="True" ...
		```
	  - **Custom template colum**   
		```
		<control:FilterDataGrid.Columns>   
		    <control:DataGridTemplateColumn IsColumnFiltered="True" FieldName="LastName" ...
		```
		> **FieldName** of **DataGridTemplateColumn** is mandatory   
 - You can change the **language** in the constructor of the "Loc.cs" file (English by default)   
		`Language = (int)Local.English;`      
		Languages available : English, French, Russian, German, Italian, Chinese
> The translations are from google translate, if you find any errors please let me know.
