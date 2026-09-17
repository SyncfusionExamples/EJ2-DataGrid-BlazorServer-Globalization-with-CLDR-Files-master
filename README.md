# Blazor DataGrid – Globalization and Localization Using CLDR Data

## Overview
This sample demonstrates how to localize the Syncfusion Blazor DataGrid (`EjsGrid`) for a non-English culture using CLDR (Unicode Common Locale Data Repository) data. The grid is configured for the German (`de`) culture: order dates render using the German date format and the Freight column is formatted and displayed as currency in Euros (EUR). This pattern is commonly needed in line-of-business Blazor applications that must present grid data correctly for users in different regions and cultures.

## Key Features
- Loads German locale resource strings from `de.json` using `LoadLocaleData`.
- Loads culture-specific CLDR JSON data — numbering systems, Gregorian calendar, number formats, time-zone names, and currency data — using `LoadCldrData`.
- Applies the active grid culture at runtime with `SetCulture("de")`.
- Sets the currency code to EUR with `SetCurrencyCode("EUR")` so currency columns render using German currency conventions.
- Grid columns showcase date formatting (`Format="yMd"`) and currency formatting (`Format="C2"`), both driven by the loaded CLDR data.
- Standard DataGrid features (sorting, grouping, paging) remain enabled alongside the localization setup.

## Prerequisites
- Visual Studio 2022 or later or Visual Studio Code
- .NET SDK compatible with the project's target framework

## How to Run the Project

**Visual Studio 2022**

1. Clone or download this repository to your local machine.
2. Open `BlazorApp1/BlazorApp1.sln` in Visual Studio 2022.
3. Restore NuGet packages (Visual Studio typically does this automatically on first build; otherwise right-click the solution and choose **Restore NuGet Packages**).
4. Build the solution.
5. Run the project (**F5** or **Ctrl+F5**). The app opens in your default browser.
6. On the home page, confirm the DataGrid loads with German culture formatting applied — the **Order Date** column should use the German date pattern, and the **Freight** column should display values with the € symbol.

**Visual Studio Code**

1. Open the repository folder in Visual Studio Code.
2. Open the integrated terminal.
3. Navigate to the project directory.

```bash
dotnet restore
dotnet run
```

## Project Structure
- `BlazorApp1/Pages/Index.razor` — hosts the `EjsGrid` component and contains the logic that loads the locale/CLDR data and applies the German culture and currency settings.
- `BlazorApp1/wwwroot/de.json` — German locale resource file consumed by `LoadLocaleData`.
- `BlazorApp1/wwwroot/cldr-data/` — CLDR data files (`main-de`, `segments-de`, `supplemental`) consumed by `LoadCldrData`.
- `BlazorApp1/wwwroot/sample-data/` — sample data used to populate the grid.

## Support and Feedback
- For general product questions, visit the [Syncfusion Community Forum](https://www.syncfusion.com/forums) or [Syncfusion Support](https://www.syncfusion.com/support).
- To report an issue specific to this sample, open a GitHub issue in this repository.
- Full documentation on Blazor DataGrid globalization and localization: https://help.syncfusion.com/grid-sdk/blazor/data-grid/global-local

## License
This is a Syncfusion sample project provided to demonstrate product usage. Review the [Syncfusion license terms](https://www.syncfusion.com/sales/pricing?category=ui-components) before using Syncfusion components in your own applications.
