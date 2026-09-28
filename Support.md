# Arigin Support

Version: 1.0.0  
Developer: Hu Dongsheng (胡冬生)  
Email: [hudongsheng356@gmail.com](mailto:hudongsheng356@gmail.com)

Arigin brings worksheets, scientific graphs, and data analysis into one workspace. Start with an included sample or import your own data.

## Getting started

Choose New Workspace, Open Workspace…, or Load Sample on the launch screen. Use Worksheet, Graph, and Results to switch pages. The inspector contains Data & Layers, Appearance, and Fit & Calculate.

Change the interface language from the launch screen, the Arigin menu, or Settings. Options include System, 简体中文, and English.

## Frequently asked questions

### Why is my curve missing?

Check your X and Y column selections and confirm that values are numeric. Basic curves require valid X/Y pairs. Masked points are excluded from normal plotting, and logarithmic axes display positive values only. Bubble plots also require a nonnegative area column. Statistical distribution plots use valid Y values without requiring populated X cells.

### Why can’t I pan or zoom some plot types?

Histograms, density plots, empirical CDFs, box plots, violins, rug plots, Q–Q plots, horizontal bars, pies, donuts, polar plots, and 2D waterfalls use their own automatic rendering. In this version, they do not provide the basic plots’ gesture navigation, dual Y axes, error bars, fit overlays, or multiple panels.

### Which files can I import?

Arigin reads UTF-8 CSV and TSV, XLSX, and supported MAT, OPJ, and OPJU data structures. Legacy XLS, MAT v7.3, and unrecognized project encodings are not fully supported.

XLSX formulas use cached results stored in the file. Arigin does not execute spreadsheet formulas, macros, or external links. If cached results are missing, recalculate and save the workbook in its original spreadsheet application.

OPJ / OPJU support focuses on recognized numeric data. It does not guarantee restoration of every original layout, analysis object, script, or column property. For unsupported files, export UTF-8 CSV / TSV first, or email a small, nonconfidential example to support.

### Why did fitting fail or produce an unexpected result?

Check the valid point count, initial parameters, constraints, and model choice. Weighted fitting requires positive, finite values in the selected Y-error column. Convergence alone does not establish model suitability; inspect residuals, data ranges, and the report.

### How do I set a figure’s physical size?

Open Appearance → Canvas & Frame and enable Fixed Canvas Size. Enter width and height in centimeters. For a figure 9 cm wide and 15 cm high, enter 9 and 15 respectively. Follow your target publication’s actual size requirements.

### How do I save or export?

Use the system Save command to keep an editable workspace. Use Export to create PDF, PNG, BMP, TIFF, or JPEG files. Copy Figure places the current figure on the clipboard. Exported images do not replace your editable workspace.

### Does masking delete my data?

No. Masking retains original values while excluding affected points from the relevant calculations. X masks affect curves that use that X column; Y masks affect that column. Use the masking tools to restore points.

### Can one dataset have several analyses?

Yes. New analysis views reuse the current worksheet data while keeping separate graph settings and analysis records. Editing shared data affects other views using it, and saved fits may need to be rerun.

## Reporting an issue

Suggested subject: Arigin 1.0.0 — Short issue summary.

Include your app version, system version, steps to reproduce, expected result, and actual result. For import issues, include the file extension. Screenshots and small examples with confidential information removed are helpful. Do not send passwords or files you are not authorized to share.

Support is handled by the developer; no fixed response time is promised. For privacy matters, include “Privacy Request” in the email subject.
