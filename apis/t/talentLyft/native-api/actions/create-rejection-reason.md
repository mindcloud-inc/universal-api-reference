# Create Rejection Reason with TalentLyft

Creates a new rejection reason in TalentLyft.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/rejection_reasons`
- **Base URL:** `https://api.talentlyft.com`
- **Official documentation:** [Create Rejection Reason](https://developers.talentlyft.com/customer-api-reference/rejection-reasons)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Name` | body | `string` | yes | The rejection reason name. |
| `Type` | body | `string` | no | The rejection reason type. |
