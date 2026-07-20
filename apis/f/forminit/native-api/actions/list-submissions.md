# List Submissions with Forminit

Retrieves submissions for a specific Forminit form.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/forms/:formId`
- **Base URL:** `https://api.forminit.com`
- **Official documentation:** [List Submissions](https://forminit.com/docs/list-submissions-api/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `string` | yes | Form identifier to read submissions from. |
| `query` | query | `string` | no | Search term used to filter matching submissions. |
| `files` | query | `boolean` | no | Include file details in the response when true. |
| `timezone` | query | `string` | no | IANA timezone used for formatted submission dates. |
