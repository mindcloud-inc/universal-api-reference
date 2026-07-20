# Update Lead with MailBluster

Updates an existing lead in MailBluster by lead hash.

## Endpoint

- **Method:** `PUT`
- **Path:** `/leads/:leadHash`
- **Base URL:** `https://api.mailbluster.com/api`
- **Official documentation:** [Update Lead](https://app.mailbluster.com/api-doc/leads/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `leadHash` | path | `string` | yes | MD5 hash of the lead email to update. |
| `firstName` | body | `string` | no | Updated first name of the lead. |
| `lastName` | body | `string` | no | Updated last name of the lead. |
| `subscribed` | body | `boolean` | no | Updated subscribed status. |
