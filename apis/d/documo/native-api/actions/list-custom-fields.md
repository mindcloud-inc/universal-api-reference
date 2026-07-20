# List Custom Fields with Documo

Retrieves custom field records from Documo.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/custom-fields`
- **Base URL:** `https://api.documo.com`
- **Official documentation:** [List Custom Fields](https://docs.documo.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `entity` | query | `string` | no | Entity type to filter by. Possible values: fax, account, user. |
