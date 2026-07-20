# Issue Badge to Recipient with IssueBadge

## Endpoint

- **Method:** `POST`
- **Path:** `/issue/create`
- **Base URL:** `https://app.issuebadge.com/api/v1`
- **Official documentation:** [Issue Badge to Recipient](https://app.issuebadge.com/docs/api-documentation.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `badge_id` | body | `string` | yes | Encrypted badge ID from badge creation |
| `name` | body | `string` | yes | Recipient full name Maximum length: 200. |
| `email` | body | `string` | no | Recipient email address |
| `phone` | body | `string` | no | Recipient phone number |
| `idempotency_key` | body | `string` | yes | Unique key to prevent duplicate issuance Maximum length: 100. |
| `metadata` | body | `object` | no | Custom field values and additional metadata |
