# Create Emails with Bento Now

Queues transactional emails in Bento Now.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/batch/emails`
- **Base URL:** `https://app.bentonow.com/api`
- **Official documentation:** [Create Emails](https://bentonow.com/docs/emails_api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `emails[].from` | body | `string` | yes |
| `emails[].html_body` | body | `string` | yes |
| `emails[].subject` | body | `string` | yes |
| `emails[].to` | body | `string` | yes |
| `emails[].transactional` | body | `boolean` | yes |
