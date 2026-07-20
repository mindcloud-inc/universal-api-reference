# Run localized advanced report with Rakuten Advertising

Retrieves a localized advanced report from Rakuten Advertising.

## Endpoint

- **Method:** `GET`
- **Path:** `/advancedreports/1.0`
- **Base URL:** `https://api.linksynergy.com`
- **Official documentation:** [Run localized advanced report](https://developers.rakutenadvertising.com/documentation/en-US/affiliate_apis/advanced_reports)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bdate` | query | `string` | yes | Report begin date in YYYYMMDD format. |
| `edate` | query | `string` | yes | Report end date in YYYYMMDD format. |
| `lang` | query | `string` | no | Report language code. |
| `locale` | query | `string` | no | Report locale code. |
