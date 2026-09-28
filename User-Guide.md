# Arigin User Guide

Version: 1.0.0  
Developer: Hu Dongsheng (胡冬生)  
Email: [hudongsheng356@gmail.com](mailto:hudongsheng356@gmail.com)

## 1. Create your first workspace

The launch screen offers three choices:

- New Workspace starts with an empty worksheet.
- Open Workspace… opens a saved workspace or supported data file.
- Load Sample provides curve, peak-fitting, and surface examples.

A workspace can contain several worksheets. A worksheet holds the source data; analysis views keep different graph and analysis states for the same worksheet.

## 2. Find your way around

Select a worksheet in the sidebar. Worksheet, Graph, and Results switch between data editing, plotting, and reports. The inspector has three sections:

- Data & Layers: X/Y/Z assignments, plot types, curves, and layouts.
- Appearance: canvas, frame, axes, grid, colorbar, curves, legend, and text.
- Fit & Calculate: models, initial values, constraints, and fitting options.

Use the inspector button to show or hide the panel. When space is limited, scroll the graph toolbar horizontally to reach additional actions.

## 3. Import and organize data

Choose Import Data or edit worksheet cells directly. Column tools manage names, units, and roles. Row tools append, insert, delete, or clear rows. Paste into Range… places clipboard data at a chosen starting row and column.

Supported inputs include UTF-8 CSV / TSV, XLSX, and recognized MAT and OPJ / OPJU numeric structures. XLSX formulas depend on saved cached results. Legacy XLS and MAT v7.3 are unsupported. OPJ / OPJU import does not restore every original graph or analysis object.

Basic curves use valid X/Y pairs. Empty, nonnumeric, and masked values are generally excluded from the relevant calculations. Do not replace missing values with zero unless zero is genuinely the intended measurement.

## 4. Choose a plot

Open Graph, select X and Y in Data & Layers, and choose a plot type. The Plot Type toolbar menu offers the same choices.

1. Basic: line + symbol, scatter, line, step, stem, column, horizontal bar, area, and bubble.
2. Distributions: histogram, kernel density, empirical CDF, box, violin, rug, and normal Q–Q.
3. Specialty: pie, donut, polar, and 2D waterfall.

Bubble plots require an additional area column. Statistical plots use valid Y values and do not require populated X cells. Pie and donut charts use numeric X categories and positive Y shares. Polar plots interpret X as degrees and Y as a nonnegative radius, connecting points in row order.

Box plots use 1.5 IQR whiskers and display outside observations separately. Violins show a kernel density estimate with automatic bandwidth. Density estimation is not a fitted model or a significance test.

## 5. Multiple curves, dual axes, and panels

For basic plots, enable Multiple Curves and select the Y columns to display. Edit each curve’s color, width, line style, and symbols under Appearance → Curves & Legend.

In Single layout, Right Y Data adds a curve sharing X with an independent right Y scale. Edit that scale under Right Y in the axis editor. Without dual Y axes, choose top or bottom for X and left or right for Y.

Basic plots can use multiple panels with shared X/Y ranges. Box, violin, and 2D waterfall plots also support selected multiple Y columns, but do not use the basic plots’ panel mechanism.

## 6. Reuse a dataset

Use the Analysis View menu to create a new view or duplicate the current one. Each view retains its plot type, column selections, appearance, and analysis records while sharing the worksheet’s source data.

For example, keep a line-and-symbol fit in one view and a histogram of the same Y column in another. Editing shared values or masks affects all views using them. Saved results are calculation snapshots; rerun analysis when needed.

## 7. Edit axes, grids, and text

Basic plots support manual axis ranges and automatic ranges. Drag or use two-finger scrolling to pan; pinch, use the wheel, or use modified scrolling to zoom. Logarithmic axes display positive values only.

With on-plot editing enabled, double-click supported titles, axis titles, legends, or the plot area to open the corresponding inspector settings. With editing disabled, double-clicking a basic plot resets its viewport.

Grid & Colorbar controls the applicable major/minor grids, line styles, colors, and widths. Colorbars apply to 3D scatter, surfaces, and contours. Curves & Legend can adjust curve styles or legend samples separately.

Text & Labels provides title text, font, size, and color controls. Rich text supports bold, italic, underline, superscript, subscript, and common Greek characters. Basic 2D plots can include coordinate-based text annotations.

The newer distribution and specialty plots use automatic coordinates. They do not provide gesture navigation, dual Y axes, error bars, fit overlays, multiple panels, or coordinate text annotations. Their Cartesian plots support titles, axis positions, major grids, and frames; minor grids and custom spacing remain available in the original basic plots. Pie and donut charts use automatic category colors.

## 8. Fit and analyze

After selecting X/Y, open Fit & Calculate. Arigin provides first- through third-degree polynomials, 16 built-in nonlinear models, and custom functions.

The nonlinear models are Gaussian, Lorentzian, exponential decay, exponential growth, double exponential decay, power law, logarithmic, Logistic, Boltzmann, sine, cosine, damped sine, Michaelis–Menten, Hill, Gompertz, and stretched exponential.

Set initial values, fixed parameters, and bounds as needed. Y-error weighting requires positive finite errors for every valid fit point. Custom functions use named parameters and numerical expressions, not arbitrary scripts.

Inspect the report, R², and residuals after fitting. Residuals can be written to a new column. Parameter confidence intervals are not available in this version. Convergence does not establish that a model is appropriate for the scientific question.

The Analysis menu also provides descriptive statistics, integration, differentiation, smoothing, and data processing. Processing tools include column formulas, sorting/filtering, normalization, baseline subtraction, interpolation, peak finding, correlation, histogram binning, and FFT. FFT requires uniform valid sampling and does not automatically fill masked gaps.

Batch fitting supports independent or concatenated fits. Workflows can recalculate supported derived columns and single-curve fits in dependency order.

## 9. Mask and restore points

Use point selection, rectangular selection, row numbers, or cross-column masking to exclude points. Masking keeps original values. Restore masks when needed; supported edits can be undone.

X masks affect curves using that X column, while Y masks affect the corresponding column. Grubbs and Dixon tests require suitable data and assumptions. Review the report before masking a candidate.

## 10. Explore 3D and contours

Load the surface sample or choose valid X, Y, and Z columns. Select 3D layout, then 3D Scatter, Surface, or Contour (2D).

Surfaces and contours require a complete regular grid with one valid Z for each X/Y pair. Use 3D scatter for incomplete grids. Drag to rotate the 3D view. Metal accelerates interactive rendering when available; exports use the figure export workflow.

## 11. Size, save, and export

Enable Fixed Canvas Size under Canvas & Frame. Enter width and height in centimeters, such as 9 cm wide by 15 cm high. This example is not a universal journal standard; follow the target publication’s requirements.

Styles → Presets offers Publication and Presentation presets. You can also copy, save, and load graph styles. Choose suitable fonts, line widths, and legend layouts for small canvases.

Save an editable workspace with the Save command. Export supports PDF, PNG, BMP, TIFF, and JPEG, with physical size and applicable resolution settings. PDF uses a vector export path; this does not guarantee that every layer in every plot is a pure vector object. Check the exported text, legend, and frame.

Copy Figure places a bitmap on the clipboard for pasting into a document. CSV exports share data. Exporting a figure does not replace saving the workspace.

## 12. Language, privacy, and help

Switch languages from the launch screen, Arigin menu, or Settings. Column names, user titles, and existing reports retain their original text; newly generated reports use the current language.

Core analysis runs locally without an account. Read the Privacy Policy for file, clipboard, and support-email practices. For help, contact Hu Dongsheng at hudongsheng356@gmail.com.
