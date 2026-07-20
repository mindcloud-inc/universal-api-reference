# Create List with Perfit

## Endpoint

- **Method:** `POST`
- **Path:** `/:account/lists`
- **Base URL:** `https://api.myperfit.com/v2`
- **Official documentation:** [Create List](https://developers.myperfit.com/contacts-api/introduccion)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account` | path | `string` | yes | Perfit account name. |
| `name` | body | `string` | yes | Provisional list name field based on the generic REST create contract; confirm against the full reference before production use. |
