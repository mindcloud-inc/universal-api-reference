# Get Keyword Profile Keys By Group with Agilite

Retrieves keyword profile keys from Agilite by group.

## Endpoint

- **Method:** `GET`
- **Path:** `/keywords/getProfileKeysByGroup`
- **Base URL:** `https://api.agilite.io`
- **Official documentation:** [Get Keyword Profile Keys By Group](https://docs.agilite.io/reference/getprofilekeysbygroup)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `group-name` | query | `string` | yes | Agilit-e keyword group name. |
| `sort` | query | `string` | no | Optional sort expression supported by the Agilit-e endpoint. |
