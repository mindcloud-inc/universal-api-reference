# Create Interest with Perfit

## Endpoint

- **Method:** `POST`
- **Path:** `/:account/interests`
- **Base URL:** `https://api.myperfit.com/v2`
- **Official documentation:** [Create Interest](https://developers.myperfit.com/contacts-api/introduccion)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account` | path | `string` | yes | Perfit account name. |
| `name` | body | `string` | yes | Interest name. |
