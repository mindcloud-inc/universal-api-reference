# Create Webhook with SignRequest

## Endpoint

- **Method:** `POST`
- **Path:** `/webhooks/`
- **Base URL:** `https://signrequest.com/api/v1`
- **Official documentation:** [Create Webhook](https://signrequest.com/api/v1/docs/#operation/webhooks_create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | Maximum length: 255. |
| `event_type` | body | `list<string>` | yes | Accepted values: `cancelled`, `convert_error`, `converted`, `declined`, `downloaded`, `expired`, `login_failed`, `login_successful`, `password_reset_request_error`, `password_reset_request_sent`, `sending_error`, `sent`, `signed`, `signer_downloaded`, `signer_email_bounced`, `signer_forwarded`, `signer_signed`, `signer_viewed`, `signer_viewed_email`, `signrequest_received`, `viewed`. |
| `callback_url` | body | `string` | yes | Maximum length: 2100. |
| `integration` | body | `list<string>` | no | Accepted values: `formdesk`, `mfiles`, `microsoft-flow`, `salesforce`, `zapier`. |
