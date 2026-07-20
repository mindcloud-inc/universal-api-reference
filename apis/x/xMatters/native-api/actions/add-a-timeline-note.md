# Add a timeline note with xMatters

Adds a timeline note in your xMatters instance.

## Endpoint

- **Method:** `POST`
- **Path:** `incidents/{incidentId}/timeline-entries`
- **Base URL:** `https://mindcloud.xmatters.com/api/xm/1`
- **Official documentation:** [Add a timeline note](https://help.xmatters.com/xmapi/index.html#add-a-timeline-note)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `entryType` | body | `string` | no |
| `incidentId` | path | `string` | no |
| `text` | body | `string` | no |
