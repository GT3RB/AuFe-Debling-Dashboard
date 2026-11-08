# PROJECT: INTERACTIVE GEOLOGY & MINING OPERATIONS DASHBOARD

## 1. ROLE AND OBJECTIVE

Act as a senior Front-End Developer, UI/UX Designer, and Data Visualisation Specialist.

Your task is to design and develop a professional, interactive **Mining Geology & Operations Dashboard** using HTML, CSS, and JavaScript.

The dashboard will be used to visualise and monitor information across three major divisions:

1. Geology Division
2. Operations Division
3. Safety Division

The dashboard must use the supplied Excel workbook, `Master Datasheet.xlsx`, as its primary data source.

The objective is to create a modern, professional, functional, and visually appealing dashboard that makes complex mining information easy to understand, navigate, and interpret.

This must be a working dashboard, not merely a static UI mockup.

---

## 2. PROJECT STRUCTURE AND FIRST IMPRESSIONS

### Welcome Screen

When the dashboard is opened for the first time, the user must be greeted by a dedicated welcome screen.

The welcome screen should include:

- A professional dashboard title, such as "Mining Operations Dashboard".
- A short welcome message.
- A clean and professional visual layout.
- Three clearly distinguishable division cards.
- A suitable icon or visual identifier for each division.

The three division options must be:

**1. Geology Division**
- Represents blast-hole information, grade distribution, bench information, and geological statistics.

**2. Operations Division**
- Represents mining truck movements, material transportation, tonnes hauled, and cycle times.

**3. Safety Division**
- Represents safety incidents, risk assessments, incident descriptions, and corrective actions.

When the user clicks on a division card, they should be taken directly to the corresponding dashboard.

Provide a navigation option to return to the welcome screen from any division.

---

## 3. DIVISION REQUIREMENTS

### A. GEOLOGY DIVISION

Develop an interactive Geology Dashboard that displays geological information for different mining benches.

#### Bench Selector

At the top of the dashboard, provide an interactive Bench Selector with four options:

- Bench 240
- Bench 245
- Bench 250
- All Benches

Selecting an option must dynamically update all geological statistics, visualisations, and tables.

The "All Benches" selection must combine the data from all three geology worksheets without duplicating records.

#### Key Performance Indicators (KPIs)

Display the following information prominently:

1. Total Number of Blast Holes
   - Count the number of recorded blast holes.

2. Average Grade
   - Calculate the arithmetic average grade.
   - Display the result in grams per tonne (g/t).

3. High Grade Distribution
   - Calculate the percentage of blast holes classified as High Grade.

4. Medium Grade Distribution
   - Calculate the percentage classified as Medium Grade.

5. Waste Distribution
   - Calculate the percentage classified as Waste.

6. Maximum Grade
   - Display the highest recorded grade in g/t.
   - Where possible, identify the corresponding blast-hole ID.

#### Additional Geological Information

Include additional useful geological information where appropriate:

- Minimum recorded grade.
- Total High Grade, Medium Grade, and Waste blast-hole counts.
- Average Relative Level (RL).
- Minimum and maximum RL.
- Grade distribution across the selected bench.
- Geological grade distribution chart.
- Blast-hole identification and grade information.

#### Visualisations

Include suitable interactive charts, such as:

- Doughnut chart showing High Grade, Medium Grade, and Waste percentages.
- Bar chart displaying grade distribution.
- A geological blast-hole location plot using the Latitude and Longitude values.
- A detailed blast-hole data table.

The geological location plot should allow users to identify individual blast holes and inspect relevant information, including their ID, grade, category, and RL.

A simple interactive SVG or Canvas scatter plot is acceptable. Do not require an external mapping API.

#### Blast-Hole Data Table

Display the available blast-hole information:

- Blasthole ID
- Bench Number
- RL (m)
- Latitude
- Longitude
- Grade (g/t)
- Grade Category

Add search, sorting, and category filtering.

Use readable category names in the interface:

- HG = High Grade
- MG = Medium Grade
- W = Waste

---

### B. OPERATIONS DIVISION

Develop an Operations Dashboard for monitoring mining truck activities.

#### Truck Selector

At the top of the dashboard, provide a Truck ID Selector.

The selector must contain all available truck IDs from the supplied workbook.

Selecting a truck must dynamically display its corresponding operational information.

Also provide an "All Trucks" option to view combined operational information.

#### Key Performance Indicators

Display useful operational statistics, including:

1. Total Loads
2. Total Tonnes Transported
3. Average Tonnes Per Load
4. Average Cycle Time (minutes)
5. Shortest Cycle Time
6. Longest Cycle Time

All calculations must update according to the selected truck or All Trucks selection.

#### Individual Truck Information

Display the following information for each recorded load:

- Truck ID
- Load Location
- Load Time
- Material Type
- Dump Location
- Dump Time
- Tonnes Per Load
- Cycle Time (mins)

#### Additional Operational Information

Include useful operational insights where supported by the source data:

- Distribution of transported material.
- Total tonnes transported by material type.
- Loads by truck.
- Loads by loading location.
- Loads by dumping location.
- Cycle-time comparison between trucks.

#### Visualisations

Include suitable charts, such as:

- Bar chart comparing total tonnes transported by each truck.
- Doughnut chart showing material distribution.
- Bar chart showing average cycle time by truck.
- Operational load history table.

Provide sorting, filtering, and searching functionality for the load records.

Important: Only display material types that actually exist in the workbook. Do not invent Medium Grade operational loads.

---

### C. SAFETY DIVISION

Develop a Safety Dashboard for monitoring and investigating recorded safety incidents.

#### Incident ID Selector

Provide an interactive Incident ID Selector containing all available Incident IDs.

Selecting an incident must display the corresponding incident information.

The selector should also support searching for an incident by its ID.

#### Incident Information

Display the following information for the selected incident:

1. Incident ID
2. Date Occurred
3. Area
4. Event Type
5. Category
6. Description
7. Potential Risk
8. Actual Outcome
9. Lost Time Injury (Yes/No)
10. Action Taken

Descriptions and actions must be displayed in full without unnecessarily cutting off important information.

#### Additional Safety Information

Include useful safety statistics and insights:

- Total Recorded Incidents.
- Total Lost Time Injuries.
- Incidents Without Lost Time Injury.
- Incidents by Event Type.
- Incidents by Area.
- Incidents by Category.
- Potential Risk distribution.
- Incident trends over time.

#### Visualisations

Include appropriate charts, such as:

- Doughnut chart showing incident distribution by Event Type.
- Bar chart showing incidents by Area.
- Chart showing incidents by Category.
- Incident timeline or monthly trend chart.

#### Incident Search and Filtering

Allow users to filter incident records by:

- Incident ID
- Event Type
- Area
- Category
- Lost Time Injury status

Use clear visual indicators for incident risk levels and Lost Time Injury status.

The incident detail view should be organised into readable sections, making it easy to understand what happened, the potential consequences, the actual outcome, and the corrective action taken.

---

## 4. EXCEL WORKBOOK AND DATA SPECIFICATIONS

The supplied workbook, `Master Datasheet.xlsx`, is the authoritative source of dashboard information.

Read all five worksheets and use their actual data.

Do not replace the supplied data with fictional examples, placeholder records, or generic mining statistics.

### Worksheet 1: Geo_Data_Bench240

Contains 42 blast-hole records for Bench 240.

Columns:

- Blasthole_ID
- Bench #
- RL (m) - height above sea level
- Latitude
- Longitude
- Grade (grams/tonne)
- Grade_category

### Worksheet 2: Geo_Data_Bench245

Contains 42 blast-hole records for Bench 245.

Uses the same column structure as Bench 240.

### Worksheet 3: Geo_Data_Bench250

Contains 42 blast-hole records for Bench 250.

Uses the same column structure as the other geological worksheets.

### Worksheet 4: Ops_Data

Contains 80 operational load records involving 10 different trucks.

Columns:

- Truck ID
- Load Location
- Load Time
- Material Type
- Dump Location
- Dump Time
- Tonnes Per Load
- Cycle Time (mins)

Available truck IDs range from TRK-01 to TRK-10.

Available load locations:
- North Pit
- South Pit

Available material types:
- High Grade Gold
- Waste

Available dump locations:
- ROM Pad
- Waste Dump

Important: Load Time and Dump Time are stored as Excel time fractions. Convert these into properly formatted 24-hour clock values (HH:mm).

Do not interpret these time values as complete dates or invent missing operational dates.

### Worksheet 5: Safety_Data

Contains 97 safety incident records.

Columns:

- Incident ID
- Date
- Area
- Event Type
- Category
- Description
- Potential Risk
- Actual Outcome
- Lost Time Injury
- Action Taken

Incident IDs range from INC-001 to INC-097.

The Date column contains Excel date serial values. Convert these into correctly formatted dates without introducing timezone-related date shifts.

Display dates in a consistent readable format, such as DD MMM YYYY.

### Data Handling Rules

- Use the workbook as the single source of truth.
- Preserve all original records.
- Do not silently modify or reinterpret the source data.
- Do not invent missing values or categories.
- Calculate all KPIs dynamically using JavaScript.
- Ensure that the "All" selections combine the relevant datasets correctly.
- Ensure that category percentages use the correct total number of records as their denominator.
- Handle missing or invalid values gracefully.
- Retain the original source identifiers when displaying records.
- Use appropriate rounding for displayed numerical values without changing the underlying calculations.

---

## 5. ADDITIONAL FUNCTIONAL REQUIREMENTS

Make the dashboard more useful by implementing the following functionality.

### Navigation

- Welcome screen as the initial landing page.
- Navigation between all three divisions.
- Clearly visible Back to Home functionality.
- Indication of the currently selected division.
- Consistent navigation throughout the application.

### Interactivity

- Working dropdown selectors.
- Dynamic KPI calculations.
- Interactive charts.
- Search functionality.
- Sorting and filtering.
- Table pagination or a manageable scrollable table where appropriate.
- Reset Filters functionality.
- Informative empty states when no records match the filters.

### Data Export

Where practical, provide an Export to CSV function for filtered data tables.

The exported information should reflect the currently selected filters.

### User Experience

- Provide appropriate tooltips for charts and metrics.
- Use clear labels and measurement units.
- Highlight important statistics.
- Ensure the dashboard is easy to operate without requiring technical knowledge.
- Avoid unnecessary animations or distracting visual effects.
- Provide clear feedback when users change selectors or filters.

---

## 6. UI/UX AND VISUAL DESIGN REQUIREMENTS

Use the supplied reference image as the primary visual design inspiration.

Study its layout, spacing, colours, typography, component placement, and overall design language.

Create a dashboard that follows the visual direction of the reference while ensuring that all three divisions have a consistent design.

### Design Principles

- Modern and professional.
- Clean and minimal.
- Organised information hierarchy.
- Consistent spacing and alignment.
- Clear visual distinction between sections.
- Easy-to-read charts and statistics.
- Visually appealing without unnecessary decoration.

### Colour Scheme

Use a sensible mining-industry-inspired colour palette.

Suggested direction:

- Dark charcoal or navy for navigation and primary interface elements.
- Gold or amber for geological information and important highlights.
- Teal or blue for operational information.
- Appropriate green, amber, and red indicators for safety information.
- Neutral backgrounds for data tables and content areas.

Maintain consistency throughout the dashboard.

### Typography

Use professional, readable typography.

Ensure:

- Headings are clearly distinguishable.
- KPI values are prominent.
- Supporting descriptions are readable.
- Tables are easy to scan.
- Font sizes are consistent.

### Dashboard Layout

Use a sensible layout featuring:

- Header and navigation.
- Division title and description.
- Filter and selector section.
- KPI cards.
- Charts and visualisations.
- Detailed data tables.

The layout should make good use of available screen space without overcrowding the interface.

### Responsive Design

The dashboard must work across:

- Desktop computers.
- Laptops.
- Tablets.
- Mobile devices.

Ensure that cards, charts, tables, selectors, and navigation adapt appropriately to smaller screens.

---

## 7. TECHNICAL REQUIREMENTS

### Development Technology

Build the complete dashboard using:

- HTML5
- CSS3
- Vanilla JavaScript

CSS and JavaScript must be included inside the HTML document using appropriate `<style>` and `<script>` sections.

### File Structure

The primary deliverable must be a single self-contained HTML file.

For example:

`Geology_Dashboard.html`

Do not require a complex development environment, Node.js installation, build process, or backend server.

### Code Quality

- Use clean and organised code.
- Use meaningful variable and function names.
- Separate data handling, calculations, rendering, and event handling into logical functions.
- Include helpful code comments.
- Avoid unnecessary code duplication.
- Ensure all interactive elements actually work.
- Avoid console errors.
- Ensure that selectors and charts update correctly when the user changes divisions or filters.

### External Dependencies

Prefer native HTML, CSS, JavaScript, SVG, and Canvas.

If an external charting library is genuinely beneficial, use a suitable lightweight library and clearly identify any internet connection requirement.

The dashboard should not depend on external APIs for its core functionality.

### Data Integration

Extract the data from the supplied Excel workbook and embed it into JavaScript data structures within the final HTML document.

The finished dashboard must work independently of the original Excel file after generation.

Do not reference an assumed local file path to the Excel workbook.

All calculations and visualisations must use the embedded workbook data.

---

## 8. DELIVERABLES

Provide the following deliverables:

### Deliverable 1: Complete HTML Dashboard

Produce one fully functional HTML file named:

`Geology_Dashboard.html`

It must contain:

- Complete HTML structure.
- Embedded CSS.
- Embedded JavaScript.
- Embedded datasets extracted from all five Excel worksheets.
- Welcome screen.
- Geology Division.
- Operations Division.
- Safety Division.
- Working selectors, charts, KPIs, filters, and tables.

### Deliverable 2: Data Integration

Ensure that all records from the supplied workbook are represented in the dashboard.

Specifically:

- 42 records from Bench 240.
- 42 records from Bench 245.
- 42 records from Bench 250.
- 80 operational records.
- 97 safety incident records.

No records should be intentionally omitted.

### Deliverable 3: Functional Testing

Test all major features before considering the project complete.

Verify that:

- The welcome screen appears on initial startup.
- All three division cards navigate correctly.
- The Bench Selector works for 240, 245, 250, and All.
- Geological KPIs update correctly.
- The Truck Selector works for individual trucks and All Trucks.
- Operational KPIs update correctly.
- The Incident ID Selector displays the correct incident.
- Safety filters work correctly.
- All charts respond to the relevant filters.
- Search and sorting work correctly.
- CSV exports contain the appropriate filtered information.
- Navigation back to the welcome screen works.
- The application works at different screen sizes.

### Deliverable 4: Code and Implementation Notes

Provide a brief explanation of:

- How the dashboard is organised.
- How the Excel data is integrated.
- How the KPI calculations work.
- Any external dependencies.
- How to save and launch the HTML file.

Also identify any limitations or features that could not be implemented.

---

## 9. FINAL EXPECTATIONS

The final result should resemble a professional mining-industry dashboard rather than a basic HTML webpage.

Prioritise functionality, accuracy, presentation, and ease of use.

Do not stop after creating the welcome screen or a basic visual layout.

All three divisions must be fully implemented.

Do not provide pseudocode, incomplete snippets, or placeholder functionality.

Before delivering the final result, review the entire application for visual inconsistencies, broken interactions, incorrect calculations, and missing records.

**The final objective is to deliver a complete, polished, responsive, and interactive Mining Geology & Operations Dashboard that can be opened and used directly in a modern web browser.**