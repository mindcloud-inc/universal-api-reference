# Delete Documents Batch with Happy SMS

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v1/protected/domain/custom-data/bulk/documents`
- **Base URL:** `https://www.api.nc`
- **Official documentation:** [Delete Documents Batch](https://www.happy.nc/docs/sms.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `queryFilter` | query | `string` | yes | RSQL filter expression selecting documents to delete. |
