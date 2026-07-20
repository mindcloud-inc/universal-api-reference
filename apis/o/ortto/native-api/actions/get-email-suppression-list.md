# Get Email Suppression List with Ortto

## Endpoint

- **Method:** `POST`
- **Path:** `/suppression-list/email/get`
- **Base URL:** `{apiBaseUrl}/v1`
- **Official documentation:** [Get Email Suppression List](https://help.ortto.com/a-836-managing-the-email-suppression-list-via-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | body | `number` | no | Maximum number of suppression-list emails to return (1-500). |
| `offset` | body | `number` | no | Number of suppression-list records to skip before returning results. |
| `sort_order` | body | `string` | no | Sort order for suppression-list results: asc or desc. |
| `sort` | body | `string` | no | Field to sort by. Ortto documents email for this endpoint. |
| `include_emails[]` | body | `array<string>` | no | Specific email addresses to include in the suppression-list response. |
