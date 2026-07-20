# Delete Lead with MailBluster

Deletes an existing lead from MailBluster by lead hash.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/leads/:leadHash`
- **Base URL:** `https://api.mailbluster.com/api`
- **Official documentation:** [Delete Lead](https://app.mailbluster.com/api-doc/leads/delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `leadHash` | path | `string` | yes | MD5 hash of the lead email to delete. |
