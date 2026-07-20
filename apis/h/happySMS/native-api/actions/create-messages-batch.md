# Create Messages Batch with Happy SMS

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/protected/domain/sms/bulk/messages`
- **Base URL:** `https://www.api.nc`
- **Official documentation:** [Create Messages Batch](https://www.happy.nc/docs/sms.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `resources[]` | body | `array<object>` | yes | Array of SMS message resources to create in bulk. |
