# Data folder

Keep **one current `.xlsx` workbook** in this folder.

The filename can be anything. The dashboard does **not** use the filename to identify the file.  
`python scripts/build.py` scans the workbook sheets and selects the table whose header row contains all required headers.

## Required headers

- `SL`
- `CODE`
- `Outlet Name`
- `Regional Head ID`
- `Regional Head HR Name`
- `Leader`
- `Regional Head Contact`
- `Zonal ID`
- `Zonal HR Name`
- `Zonal`
- `Zonal Contact`
- `Launching Date`
- `SFT`
- `Format`
- `Division`
- `District`
- `Area`
- `PNP Non PNP status`
- `Status`
- `Geo Location`
- `Location Type`
- `Location Type(Dv,Ds,T)`
- `Population Density`
- `Income level`
- `Floor type`
- `Layout shape`

The worksheet name may also change. Column order may change. Header capitalization/extra spaces are normalized during matching, but the safest refresh process is to preserve the headers exactly.

## Refresh

1. Delete the old `.xlsx` workbook from `/data`.
2. Upload the latest `.xlsx` workbook with any filename.
3. Commit to `main`.
4. GitHub Actions rebuilds and redeploys the dashboard.

If more than one matching workbook/table is present, the build intentionally stops instead of guessing.
