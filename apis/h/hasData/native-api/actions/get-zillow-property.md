# Get Zillow Property with HasData

Retrieves a Zillow property from HasData.

## Endpoint

- **Method:** `GET`
- **Path:** `/scrape/zillow/property`
- **Base URL:** `https://api.hasdata.com`
- **Official documentation:** [Get Zillow Property](https://docs.hasdata.com/apis/zillow/property)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `extractAgentEmails` | query | `boolean` | no | Extract agent email addresses when available. |
| `url` | query | `string` | yes | Zillow property URL. |
