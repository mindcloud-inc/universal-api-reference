# Get Verification List Results with MailerCheck

Retrieves verification results for a list from MailerCheck.

## Endpoint

- **Method:** `GET`
- **Path:** `/lists/:id/results`
- **Base URL:** `https://app.mailercheck.com/api`
- **Official documentation:** [Get Verification List Results](https://developers.mailercheck.com/email)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Verification list identifier. |
| `result` | query | `string` | no | Filter results by verification outcome. |
| `limit` | query | `number` | no | Maximum number of result rows to return. |
| `page` | query | `number` | no | Results page number. |
