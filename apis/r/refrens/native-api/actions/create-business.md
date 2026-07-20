# Create Business with Refrens

## Endpoint

- **Method:** `POST`
- **Path:** `/businesses`
- **Base URL:** `https://api.refrens.com`
- **Official documentation:** [Create Business](https://www.refrens.com/api/docs/business/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | — |
| `country` | body | `string` | yes | — |
| `auth` | body | `object` | yes | Object containing auth.email array of users to add to the business. |
| `billedTo` | body | `object` | no | — |
