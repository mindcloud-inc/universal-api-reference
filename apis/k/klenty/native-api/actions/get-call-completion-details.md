# Get Call Completion Details with Klenty

Retrieves call completion details from Klenty.

## Endpoint

- **Method:** `GET`
- **Path:** `/calls`
- **Base URL:** `https://api.klenty.com/apis/v1/user/{username}`
- **Official documentation:** [Get Call Completion Details](https://support.klenty.com/en/articles/8193357-klenty-s-get-api-s#h_b505b443a1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `endDate` | query | `string` | yes | End date for the call report window. Use yyyy-mm-dd. |
| `page` | query | `string` | no | Page number for paginating call completion results. |
| `startDate` | query | `string` | yes | Start date for the call report window. Use yyyy-mm-dd. |
