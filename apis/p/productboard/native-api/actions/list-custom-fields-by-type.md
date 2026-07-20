# List Custom Fields by Type with Productboard

Retrieves custom fields for a Productboard hierarchy type.

## Endpoint

- **Method:** `GET`
- **Path:** `/hierarchy-entities/custom-fields`
- **Base URL:** `https://api.productboard.com`
- **Official documentation:** [List Custom Fields by Type](https://developer.productboard.com/reference/getcustomfields)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | query | `string` | yes | Field type filter for Productboard custom fields. Allowed values: text, custom-description, number, dropdown, multi-dropdown, member. |
