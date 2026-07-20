# List Resource Strings with Transifex

## Endpoint

- **Method:** `GET`
- **Path:** `/resource_strings`
- **Base URL:** `https://rest.api.transifex.com`
- **Official documentation:** [List Resource Strings](https://developers.transifex.com/reference/get_resource-strings.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter[resource]` | query | `string` | yes | Return strings for this resource id. |
