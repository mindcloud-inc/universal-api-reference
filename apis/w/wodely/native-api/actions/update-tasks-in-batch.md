# Update Tasks in Batch with Wodely

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/tasks/bulkupdate`
- **Base URL:** `https://api.wodely.com`
- **Official documentation:** [Update Tasks in Batch](https://app.wodely.com/doc/api-documentation.html#update-task-batch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskGuidList` | body | `string` | yes | Provide one or more Task IDs, separated by commas. |
| `fieldName` | body | `string` | yes | Supported fields include Priority, TaskDesc, Requirements, ExternalKey, AmountDue, DeliveryFee, ServiceTime, Capacity, Skills, TemplateId, MerchantId, AfterDateTime, BeforeDateTime, Tag1, Tag2, Tag3, Tag4, Tag5. |
| `fieldValue` | body | `string` | no | The new value to apply to the selected field. |
