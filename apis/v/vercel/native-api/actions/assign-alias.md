# Assign Alias with Vercel

Assigns an alias to a Vercel deployment.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/deployments/:id/aliases`
- **Base URL:** `https://api.vercel.com`
- **Official documentation:** [Assign Alias](https://docs.vercel.com/docs/rest-api/reference/endpoints/aliases/assign-an-alias)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `alias` | body | `string` | yes | The alias hostname to assign to the deployment. |
| `id` | path | `string` | yes | The deployment ID to assign the alias to. |
