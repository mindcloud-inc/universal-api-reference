# Upsert Timecard Batch with Viewpoint Vista

Upsert TimeCard Batch

## Endpoint

- **Method:** `POST`
- **Path:** `v1/direct/subscribers/{subscriberCode}/vista/pr/2/data/time_batches/actions/upsert`
- **Base URL:** `https://api.xchange.trimble.com/connect/`
- **API:** REST
- **Official documentation:** [Upsert Timecard Batch](https://direct-api.xchange.trimble.com/reference/post-directsubscriberssubscriber_codevistapr2datatime_batchesactionsupsert)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Co` | body | `number` | yes | Vista PR company. |
| `Mth` | body | `string` | yes | Posting month for the batch. Format: YYYY-MM-DD. |
| `PRGroup` | body | `number` | yes | Vista payroll group for the batch. |
| `PREndDate` | body | `string` | yes | Payroll period end date. Format: YYYY-MM-DD. |
| `Notes` | body | `string` | no | Optional notes for the timecard batch. Maximum length: 0. |
| `__batch` | body | `string` | no | Optional custom ID for identifying the same timecard batch across Upsert calls. |
| `__lockBatch` | body | `boolean` | no | Keep the batch locked after processing the action. Maximum length: 0. |
