# Delete Recipient with Snappy

Deletes an existing recipient from Snappy.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/recipients/{recipientId}`
- **Base URL:** `https://api.snappy.com/public-api/v2`
- **Official documentation:** [Delete Recipient](https://docs.snappy.com/reference/deleterecipientbyid)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `companyId` | query | `string` | yes |
| `recipientId` | path | `string` | yes |
