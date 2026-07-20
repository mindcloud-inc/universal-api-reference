# Update Document with Happy SMS

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v1/protected/domain/custom-data/documents/:id`
- **Base URL:** `https://www.api.nc`
- **Official documentation:** [Update Document](https://www.happy.nc/docs/sms.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Unique document identifier. |
| `resource[]` | body | `array<object>` | yes | Array of document property objects to update. |
