# Run Universal Action with MindCloud

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/universal/apps/:appSlug/actions/:actionSlug/run`
- **Base URL:** `https://connect.mindcloud.co`
- **Official documentation:** [Run Universal Action](https://connect.mindcloud.co/v2/openapi.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `actionSlug` | path | `string` | yes | Action Slug for this MindCloud v2 request. |
| `appSlug` | path | `string` | yes | App Slug for this MindCloud v2 request. |
| `arguments` | body | `object` | no | Arguments for this MindCloud v2 request. |
| `connectionId` | body | `string` | no | Connection ID for this MindCloud v2 request. |
| `fields` | body | `string` | no | Fields for this MindCloud v2 request. |
| `options` | body | `object` | no | Options for this MindCloud v2 request. |
| `sort` | body | `string` | no | Sort for this MindCloud v2 request. |
| `version` | body | `string` | no | Version for this MindCloud v2 request. |
| `where` | body | `string` | no | Where for this MindCloud v2 request. |
