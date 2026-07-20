# Update Base with NocoDB

Updates details for a base in NocoDB.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v3/meta/bases/:baseId`
- **Base URL:** `https://app.nocodb.com`
- **Official documentation:** [Update Base](https://nocodb.com/apis/v3/meta)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `baseId` | path | `string` | yes | Base identifier. |
| `title` | body | `string` | no | Title of the base. |
