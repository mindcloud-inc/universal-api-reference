# Update Event with Circle

Updates an existing event in Circle.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/admin/v2/events/[:id]`
- **Base URL:** `https://{subdomain}.circle.so`
- **Official documentation:** [Update Event](https://api.circle.so/apis/admin-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Event ID |
| `space_id` | body | `number` | yes | Event space ID (required by Circle update endpoint) |
| `event` | body | `object` | yes | Event update payload |
