# Add A New Feature Flag with Unleash

Adds a new feature flag in Unleash.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/admin/projects/{projectId}/features`
- **Base URL:** `https://us.app.getunleash.io/uspp0456`
- **Official documentation:** [Add A New Feature Flag](https://docs.getunleash.io/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `object` | yes | Required JSON request body. |
| `projectId` | path | `string` | yes | Required path parameter. |
