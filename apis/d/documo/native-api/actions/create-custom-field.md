# Create Custom Field with Documo

Creates a new custom field in Documo.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/custom-fields`
- **Base URL:** `https://api.documo.com`
- **Official documentation:** [Create Custom Field](https://docs.documo.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `label` | body | `string` | yes | String \| Required |
| `apiName` | body | `string` | yes | String \| Required |
| `entity` | body | `string` | yes | String \| Required \| Possible values: fax, account, user |
| `displayUI` | body | `boolean` | yes | Boolean \| Required |
| `displayUITable` | body | `boolean` | yes | Boolean \| Required |
| `hint` | body | `string` | yes | String \| Required |
