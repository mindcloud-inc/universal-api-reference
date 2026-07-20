# Create Documents Batch with Happy SMS

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/protected/domain/custom-data/bulk/documents`
- **Base URL:** `https://www.api.nc`
- **Official documentation:** [Create Documents Batch](https://www.happy.nc/docs/sms.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `resources[]` | body | `array<object>` | yes | Array of document resources to create in bulk. |
