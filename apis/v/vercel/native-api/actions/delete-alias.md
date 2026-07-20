# Delete Alias with Vercel

Deletes an existing alias from Vercel.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v2/aliases/:aliasId`
- **Base URL:** `https://api.vercel.com`
- **Official documentation:** [Delete Alias](https://docs.vercel.com/docs/rest-api/reference/endpoints/aliases/delete-an-alias)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `aliasId` | path | `string` | yes | The alias ID or alias string to remove. |
