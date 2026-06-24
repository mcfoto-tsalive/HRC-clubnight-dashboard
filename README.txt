HOWICK RIFLE CLUB - CLUB NIGHT DIGITAL SQUAD SHEET

FILES
- index.html = the web page for TV/mobile
- assets/hrc-logo.png = logo
- scores-template.csv = sample Google Sheets layout

GOOGLE SHEETS SETUP
1. Create a new Google Sheet called HRC Club Night.
2. Import or copy the headings and rows from scores-template.csv.
3. Required columns are:
   Detail, Date, Mound, Position, Name, Grade, Card1, Card2, Total, Status
4. You can run 5 details in the same sheet.
5. Mounds 1-8 are Upstairs. Mounds 9-16 are Downstairs.
6. Use Card1 only for one-card nights, or Card1 and Card2 for two-card nights.
7. Total can be typed manually or calculated in Google Sheets.

SUGGESTED GOOGLE SHEETS TOTAL FORMULA
In I2:
=IF(AND(G2="",H2=""),"",IF(H2="",G2,G2+H2))
Copy down all rows.

PUBLISH GOOGLE SHEET AS CSV
1. File > Share > Publish to web.
2. Choose the sheet/tab.
3. Choose CSV.
4. Copy the published CSV link.
5. Open index.html in a text editor.
6. Replace this line:
   const CSV_URL = 'scores-template.csv';
   with:
   const CSV_URL = 'YOUR GOOGLE CSV LINK HERE';

GITHUB
Upload index.html, scores-template.csv and the assets folder to your GitHub Pages repository.
Once the Google CSV link is added, you only edit scores in Google Sheets.
