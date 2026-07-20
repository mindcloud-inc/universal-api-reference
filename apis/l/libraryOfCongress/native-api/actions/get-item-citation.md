# Get Item Citation with Library of Congress

Retrieves citation formats for a Library of Congress item.

## Endpoint

- **Method:** `GET`
- **Path:** `/item/{itemId}/`
- **Base URL:** `https://www.loc.gov`
- **Official documentation:** [Get Item Citation](https://www.loc.gov/apis/json-and-yaml/requests/endpoints/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `itemId` | path | `string` | yes | The loc.gov item identifier segment, such as 2014717546. |
