# Get Refdomains History with Ahrefs

## Endpoint

- **Method:** `GET`
- **Path:** `/site-explorer/refdomains-history`
- **Base URL:** `https://api.ahrefs.com/v3`
- **Official documentation:** [Get Refdomains History](https://docs.ahrefs.com/en/api/reference/site-explorer/get-refdomains-history)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `target` | query | `string` | yes | Domain or URL to analyze. |
| `date_from` | query | `date` | yes | Start date in YYYY-MM-DD format. |
| `date_to` | query | `date` | no | End date in YYYY-MM-DD format. |
