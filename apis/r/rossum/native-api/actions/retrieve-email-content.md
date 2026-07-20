# Retrieve Email Content with Rossum

Retrieves email content from Rossum.

## Endpoint

- **Method:** `GET`
- **Path:** `/emails/:emailID/content`
- **Base URL:** `https://mindcloud.rossum.app/api/v1`
- **Official documentation:** [Retrieve Email Content](https://rossum.app/api/docs/openapi/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `emailID` | path | `number` | yes | ID of the email whose raw content should be retrieved. |
