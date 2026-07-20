# Get Keyword Values By Profile Key with Agilite

Retrieves keyword values from Agilite by profile key.

## Endpoint

- **Method:** `GET`
- **Path:** `/keywords/getValuesByProfileKey`
- **Base URL:** `https://api.agilite.io`
- **Official documentation:** [Get Keyword Values By Profile Key](https://docs.agilite.io/reference/getbyprofilekey)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `profile-key` | query | `string` | yes | Agilit-e keyword profile key. |
| `sort` | query | `string` | no | Optional sort expression supported by the Agilit-e endpoint. |
