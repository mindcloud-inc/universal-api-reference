# Get Keyword Label By Value with Agilite

Retrieves a keyword label from Agilite by profile and value key.

## Endpoint

- **Method:** `GET`
- **Path:** `/keywords/getLabelByValue`
- **Base URL:** `https://api.agilite.io`
- **Official documentation:** [Get Keyword Label By Value](https://docs.agilite.io/reference/getlabelbyvalue)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `profile-key` | query | `string` | yes | Agilit-e keyword profile key. |
| `value-key` | query | `string` | yes | Keyword value key to resolve. |
