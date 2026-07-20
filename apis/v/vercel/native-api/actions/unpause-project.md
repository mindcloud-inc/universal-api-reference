# Unpause Project with Vercel

Unpauses an existing project in Vercel.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/projects/:projectId/unpause`
- **Base URL:** `https://api.vercel.com`
- **Official documentation:** [Unpause Project](https://docs.vercel.com/docs/rest-api/reference/endpoints/projects/unpause-a-project)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | The unique project identifier |
