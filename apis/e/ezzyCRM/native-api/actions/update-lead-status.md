# Update Lead Status with EzzyCRM

## Endpoint

- **Method:** `POST`
- **Path:** `/api/updateleadstatus`
- **Base URL:** `https://ezzycrm.com`
- **Official documentation:** [Update Lead Status](https://ezzycrm.com/api/PostApiDocument.aspx#updateleadstatus)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `DealId` | body | `number` | yes | ID of the lead. |
| `DealStatus` | body | `string` | yes | Status for update of this lead. |
| `LostReasonId` | body | `number` | no | ID of the reason when lead status is Lost. |
| `Comments` | body | `string` | no | Comments for the lost lead. |
