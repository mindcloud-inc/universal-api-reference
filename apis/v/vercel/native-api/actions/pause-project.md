# Pause Project with Vercel

Pauses an existing project in Vercel.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/projects/:projectId/pause`
- **Base URL:** `https://api.vercel.com`
- **Official documentation:** [Pause Project](https://docs.vercel.com/docs/rest-api/reference/endpoints/projects/pause-a-project)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | The unique project identifier |
