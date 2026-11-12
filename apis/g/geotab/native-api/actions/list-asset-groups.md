# List Asset Groups with Geotab

## Endpoint

- **Method:** `POST`
- **Base URL:** `https://{server}/apiv1`
- **Official documentation:** [List Asset Groups](https://developers.geotab.com/myGeotab/apiReference/methods/Get/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search` | body | `object` | no | Optional asset group search criteria. |
| `search.id` | body | `string` | no | Return the asset group with this ID. |
| `search.name` | body | `string` | no | Search asset groups by name. Use % as a wildcard. |
| `search.reference` | body | `string` | no | Search asset groups by reference. Use % as a wildcard. |
| `search.includeAllTrees` | body | `boolean` | no | Include security and private-user group trees in addition to company groups. |
| `resultsLimit` | body | `number` | no | — |
| `sort` | body | `object` | no | — |
| `propertySelector` | body | `object` | no | — |
