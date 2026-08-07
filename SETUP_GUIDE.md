# Quick GitHub Setup

1. Create a **brand-new empty GitHub repository**.
   - Add README: Off
   - .gitignore: No .gitignore
   - License: None

2. Extract the dashboard ZIP on your computer.

3. Upload all extracted files/folders to the repository and commit to `main`.

4. Make sure the workflow exists at:
   `.github/workflows/deploy-pages.yml`

   If your browser/Windows hides `.github`, go to:
   **Actions → New workflow → set up a workflow yourself**
   and create `.github/workflows/deploy-pages.yml` using the YAML in `GITHUB_WORKFLOW_COPY.txt`.

5. Go to **Settings → Pages → Build and deployment → Source → GitHub Actions**.

6. Go to **Actions → Deploy Zone Distribution Dashboard**.
   Wait until both **build** and **deploy** are green.

7. Open the Pages URL shown in the deploy job or under **Settings → Pages**.

## Future Excel refresh

Only replace the `.xlsx` workbook in `/data`.

- The new workbook may have **any filename**.
- Keep the same required headers.
- Keep only one matching current workbook in `/data`.
- Commit the change.
- GitHub Actions automatically rebuilds the dashboard.

## Sorting

Every dashboard table header is clickable:
- first click = ascending
- second click = descending

Sorting is performed across the entire filtered dataset, not only the current page.
