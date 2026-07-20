# Submit Email Template For Moderation with MailoPost

Submits an email template for moderation in MailoPost.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/email/templates/:template_id/to_pending`
- **Base URL:** `https://api.mailopost.ru/v1`
- **Official documentation:** [Submit Email Template For Moderation](https://mailopost.ru/api.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `template_id` | path | `string` | yes | MailoPost template identifier. |
