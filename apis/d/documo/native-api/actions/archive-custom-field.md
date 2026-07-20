# Archive Custom Field with Documo

Archives an existing custom field in Documo.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/custom-fields/:customFieldId`
- **Base URL:** `https://api.documo.com`
- **Official documentation:** [Archive Custom Field](https://docs.documo.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customFieldId` | path | `string` | yes | String \| Required \| Custom Field UUID |
| `isArchived` | body | `boolean` | no | Boolean |
