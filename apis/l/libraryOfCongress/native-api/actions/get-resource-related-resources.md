# Get Resource Related Resources with Library of Congress

Retrieves related resources for a Library of Congress resource.

## Endpoint

- **Method:** `GET`
- **Path:** `/resource/{resourceId}/`
- **Base URL:** `https://www.loc.gov`
- **Official documentation:** [Get Resource Related Resources](https://www.loc.gov/apis/json-and-yaml/requests/endpoints/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `resourceId` | path | `string` | yes | The loc.gov resource identifier path, such as 20001931/1918-04-05/ed-1. |
