# Create Geocoding List with Geocodio

Creates a new geocoding list in Geocodio.

## Endpoint

- **Method:** `POST`
- **Path:** `/lists`
- **Base URL:** `https://api.geocod.io/v1.12`
- **Official documentation:** [Create Geocoding List](https://www.geocod.io/docs/#create-a-new-list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fields` | query | `string` | no | Optional data append fields for geocoding list results. Send multiple values as a string separated by `,`. |
| `file` | body | `file` | no | CSV, TSV, Excel, or ZIP file to upload. |
| `direction` | body | `string` | yes | Whether to forward geocode addresses or reverse geocode coordinates. Accepted values: `0`, `1`. |
| `format` | body | `string` | yes | Column format template, such as {{A}} {{B}}, {{C}} {{D}}. |
| `callback` | body | `string` | no | Optional callback URL for completion notification. |
