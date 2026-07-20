# Create Placement Test with SuperSend

Creates a new placement test in SuperSend.

## Endpoint

- **Method:** `POST`
- **Path:** `/placement-tests`
- **Base URL:** `https://api.supersend.io/v2`
- **Official documentation:** [Create Placement Test](https://docs.supersend.io/docs/placement-test)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | Default: Untitled Test. |
| `test_email_subject` | body | `string` | no | — |
| `test_email_body` | body | `string` | no | HTML body of the test email to send |
| `test_email_from` | body | `string` | no | — |
| `seed_count` | body | `number` | no | Default: 10. Range: 1 to 50. |
| `sender_id` | body | `string` | no | — |
| `auto_send` | body | `boolean` | no | Default: false. |
| `team_id` | body | `string` | no | — |
