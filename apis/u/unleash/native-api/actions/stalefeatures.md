# Mark Features As Stale / Not Stale with Unleash

Marks features as stale / not stale in Unleash.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/admin/projects/{projectId}/stale`
- **Base URL:** `https://us.app.getunleash.io/uspp0456`
- **Official documentation:** [Mark Features As Stale / Not Stale](https://docs.getunleash.io/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `object` | yes | Required JSON request body. |
| `projectId` | path | `string` | yes | Required path parameter. |
