# Update Segment with Leadboxer

Updates an existing segment in Leadboxer.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/segments/{{segmentId}}`
- **Base URL:** `https://data.leadboxer.com`
- **Official documentation:** [Update Segment](https://developers.leadboxer.com/reference/updatesegment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `segmentId` | path | `number` | yes | The segment ID. |
| `segmentName` | query | `string` | yes | The segment name. |
| `accountId` | body | `string` | yes | The Leadboxer account ID. |
| `type` | body | `string` | yes | Segment visibility type. |
| `emailView` | body | `string` | yes | Email view type. |
| `notificationType` | body | `string` | yes | Notification frequency. |
