# List Activity with MailerSend

## Endpoint

- **Method:** `GET`
- **Path:** `/activity/:domain_id`
- **Base URL:** `https://api.mailersend.com/v1`
- **Official documentation:** [List Activity](https://developers.mailersend.com/api/v1/activity#get-a-list-of-activities)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain_id` | path | `string` | yes | ID of the MailerSend domain. |
| `date_from` | query | `string` | yes | Start datetime for activity results in YYYY-MM-DD HH:mm:ss format. |
| `date_to` | query | `string` | yes | End datetime for activity results in YYYY-MM-DD HH:mm:ss format. |
