# Get Submissions List with FillFaster

Retrieves submissions for a specific FillFaster form.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/getSubmissionsList`
- **Base URL:** `https://api.fillfaster.com`
- **Official documentation:** [Get Submissions List](https://documenter.getpostman.com/view/18912453/2s8ZDVZ3UJ#480d33e7-835e-4236-bcdc-abef6a23cad1)

## Capabilities

This operation supports [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `form` | query | `string` | yes | Form identifier to list submissions for. |
| `order` | query | `string` | no | Sort direction. |
| `page` | query | `number` | no | Results page number. |
| `sort` | query | `string` | no | Field to sort submissions by. |
