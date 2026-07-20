# Get Line Status By IDs with Transport for London

Retrieves line status for selected lines in Transport for London.

## Endpoint

- **Method:** `GET`
- **Path:** `/Line/:ids/Status`
- **Base URL:** `https://api.tfl.gov.uk`
- **Official documentation:** [Get Line Status By IDs](https://api.tfl.gov.uk/swagger/ui/index.html#!/Line/Line_StatusByIds)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ids` | path | `string` | yes | Comma-separated TfL line IDs, such as victoria,circle. |
| `detail` | query | `boolean` | no | Set to true to include details of disruptions causing line status. |
