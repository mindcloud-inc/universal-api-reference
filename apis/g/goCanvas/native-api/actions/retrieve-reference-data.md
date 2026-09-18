# Retrieve Reference Data with GoCanvas

## Endpoint

- **Method:** `GET`
- **Path:** `/reference_data/:referenceDataId`
- **Base URL:** `https://www.gocanvas.com/api/v3`
- **Official documentation:** [Retrieve Reference Data](https://api.gocanvas.com/api/v3/docs#retrieve-a-reference-data)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `referenceDataId` | path | `number` | yes | — |
| `format` | query | `list<string>` | no | Use Rows with Index to retrieve the row identifiers needed for updates and deletions. Accepted values: `rows`, `rows_with_index`. |
