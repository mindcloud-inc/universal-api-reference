# Get Validation Batch Results with MailRook Email Validation

Retrieves email validation batch results from MailRook.

## Endpoint

- **Method:** `GET`
- **Path:** `/validate/list/:listId`
- **Base URL:** `https://api.mailrook.com/v1`
- **Official documentation:** [Get Validation Batch Results](https://mailrook.com/docs/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `listId` | path | `string` | yes | MailRook batch list identifier. |
