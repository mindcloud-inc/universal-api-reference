# Update Lead Stage with EzzyCRM

## Endpoint

- **Method:** `POST`
- **Path:** `/api/updateleadstage`
- **Base URL:** `https://ezzycrm.com`
- **Official documentation:** [Update Lead Stage](https://ezzycrm.com/api/PostApiDocument.aspx#updateleadstage)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `DealId` | body | `number` | yes | ID of the lead. |
| `DealStageCode` | body | `string` | yes | Stage code for update of this lead. |
