# Retrieve Historical Surplus Lines Tax Rates with Surplus Lines Tax

## Endpoint

- **Method:** `GET`
- **Path:** `/historical-rates`
- **Base URL:** `https://api.surpluslinesapi.com/v1`
- **Official documentation:** [Retrieve Historical Surplus Lines Tax Rates](https://surpluslinesapi.com/docs/#historical-rates)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `state` | query | `string` | yes | State name or two-letter abbreviation. |
| `date` | query | `string` | no | Optional historical lookup date in YYYY-MM-DD format. Leave blank to use the current date according to the human docs page. |
