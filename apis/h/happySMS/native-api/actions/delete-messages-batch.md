# Delete Messages Batch with Happy SMS

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v1/protected/domain/sms/bulk/messages`
- **Base URL:** `https://www.api.nc`
- **Official documentation:** [Delete Messages Batch](https://www.happy.nc/docs/sms.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `queryFilter` | query | `string` | yes | RSQL filter expression selecting messages to delete. |
