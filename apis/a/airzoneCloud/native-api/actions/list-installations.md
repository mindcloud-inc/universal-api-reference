# List Installations with Airzone Cloud

Retrieves confirmed user installations from Airzone Cloud.

## Endpoint

- **Method:** `GET`
- **Path:** `/installations`
- **Base URL:** `https://m.airzonecloud.com/api/v1`
- **Official documentation:** [List Installations](https://developers.airzonecloud.com/docs/web-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filterParam` | query | `string` | no | Optional installation filter field. Supported values are `mac` and `name`. |
| `filterValue` | query | `string` | no | Optional filter value used with Filter Parameter. |
