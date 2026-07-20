# Send test email with Neon

Sends a test email in Neon.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/:project_id/branches/:branch_id/auth/send_test_email`
- **Base URL:** `https://console.neon.tech/api/v2`
- **Official documentation:** [Send test email](https://api-docs.neon.tech/reference/sendneonauthtestemail)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Neon API parameter project_id |
| `branch_id` | path | `string` | yes | Neon API parameter branch_id |
| `host` | body | `string` | yes | Neon API parameter host |
| `port` | body | `number` | yes | Neon API parameter port |
| `username` | body | `string` | yes | Neon API parameter username |
| `password` | body | `string` | yes | Neon API parameter password |
| `sender_email` | body | `string` | yes | Neon API parameter sender_email |
| `sender_name` | body | `string` | yes | Neon API parameter sender_name |
| `recipient_email` | body | `string` | yes | Neon API parameter recipient_email |
