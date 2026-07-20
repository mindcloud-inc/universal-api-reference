# Update Lead with InflatableOffice

Updates an existing lead in InflatableOffice.

## Endpoint

- **Method:** `POST`
- **Path:** `/leads/:leadId`
- **Base URL:** `https://rental.software/api6`
- **Official documentation:** [Update Lead](https://rental.software/support/knowledge-base/article/api-leads)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `additionalnotes1` | body | `string` | no | Additional notes field 1. |
| `eventname` | body | `string` | no | Updated event name for the lead. |
| `leadId` | path | `string` | yes | ID of the lead to update. |
| `notes` | body | `string` | no | Updated lead notes. |
| `status` | body | `string` | no | Updated lead status name. |
