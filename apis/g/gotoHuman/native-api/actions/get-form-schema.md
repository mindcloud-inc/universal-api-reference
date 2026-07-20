# Get Form Schema with gotoHuman

Retrieves a review form schema from gotoHuman.

## Endpoint

- **Method:** `GET`
- **Path:** `/fetchSchemaForFormFields`
- **Base URL:** `https://api.gotohuman.com`
- **Official documentation:** [Get Form Schema](https://github.com/gotohuman/gotohuman-mcp-server/blob/main/README.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | query | `string` | yes | The review form ID to fetch the schema for. |
