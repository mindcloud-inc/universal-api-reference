# Send Mail with ChurchStamp

Sends campaign mail to a recipient in ChurchStamp.

## Endpoint

- **Method:** `POST`
- **Path:** `/campaign-sendmail`
- **Base URL:** `https://v2.churchstamp.com/api/1.1/wf`
- **Official documentation:** [Send Mail](https://churchstampapi.docs.apiary.io/reference/campaigns/send-mail)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaign_id` | body | `string` | yes | Unique identifier for the campaign used to send mail. |
| `first_name` | body | `string` | yes | Recipient first name. |
| `last_name` | body | `string` | yes | Recipient last name. |
| `email` | body | `string` | yes | Recipient email address. |
