# List Lists with Myphoner

Retrieves all existing lists from Myphoner.

## Endpoint

- **Method:** `GET`
- **Path:** `/lists`
- **Base URL:** `https://{subdomain}.myphoner.com/api/v2`
- **Official documentation:** [List Lists](https://www.myphoner.com/docs/api/#lists)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `locked_on_defaults` | query | `boolean` | no | Return only lists that guarantee Myphoner default fields are defined. |
