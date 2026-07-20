# List Countries with Airlabs

Retrieves country database records from Airlabs.

## Endpoint

- **Method:** `GET`
- **Path:** `/countries`
- **Base URL:** `https://airlabs.co/api/v9`
- **Official documentation:** [List Countries](https://airlabs.co/docs/countries)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `code` | query | `string` | no | Filter by country ISO 2 code. |
| `continent` | query | `string` | no | Filter by continent code, such as AF, AN, AS, EU, NA, OC, or SA. |
