# TestDino - GitHub Actions Playwright Example

This is an example project that shows how to run Playwright tests on GitHub Actions with 4 shards and upload the merged report to TestDino.

The example workflow:

- installs dependencies and Playwright browsers
- runs Playwright tests in 4 shards
- uploads blob reports from each shard
- merges the shard reports into `playwright-report/report.json`
- uploads the merged report to TestDino

Set the `TESTDINO_TOKEN` GitHub Actions secret.

Get your token from [testdino](https://app.testdino.com).

Copy this folder into the root of your repository and keep `.github/workflows/playwright.yml` in the same location.

Local commands:

```bash
npm ci
npx playwright install
npx playwright test
npx tdpw upload ./playwright-report --token="YOUR_TESTDINO_TOKEN"
```
