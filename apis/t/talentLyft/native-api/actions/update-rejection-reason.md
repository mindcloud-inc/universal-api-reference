# Update Rejection Reason with TalentLyft

Updates an existing rejection reason in TalentLyft.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v2/rejection_reasons/:id`
- **Base URL:** `https://api.talentlyft.com`
- **Official documentation:** [Update Rejection Reason](https://developers.talentlyft.com/customer-api-reference/rejection-reasons)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The TalentLyft rejection reason ID. |
| `Name` | body | `string` | no | The updated rejection reason name. |
| `Type` | body | `string` | no | The updated rejection reason type. |
