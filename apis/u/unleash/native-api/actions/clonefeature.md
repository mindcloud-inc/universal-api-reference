# Clone A Feature Flag with Unleash

Clones a feature flag in Unleash.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/admin/projects/{projectId}/features/{featureName}/clone`
- **Base URL:** `https://us.app.getunleash.io/uspp0456`
- **Official documentation:** [Clone A Feature Flag](https://docs.getunleash.io/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | Required path parameter. |
| `body` | body | `object` | yes | Required JSON request body. |
| `featureName` | path | `string` | yes | Required path parameter. |
