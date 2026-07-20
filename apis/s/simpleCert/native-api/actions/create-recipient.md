# Create Recipient with SimpleCert

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/:project_id/recipient/add`
- **Base URL:** `https://app.simplecert.net/api`
- **Official documentation:** [Create Recipient](https://simplecert.readme.io/reference/recipients-create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `number` | yes | Project identifier. |
| `FIRST_NAME` | body | `string` | yes | Recipient first name. |
| `LAST_NAME` | body | `string` | yes | Recipient last name. |
| `EMAIL_ADDRESS` | body | `string` | yes | Recipient email address. |
| `dont_send_email` | body | `string` | no | Set to true to suppress the outbound recipient email. |
