# Get Lead with MailBluster

Retrieves a lead from MailBluster by lead hash.

## Endpoint

- **Method:** `GET`
- **Path:** `/leads/:leadHash`
- **Base URL:** `https://api.mailbluster.com/api`
- **Official documentation:** [Get Lead](https://app.mailbluster.com/api-doc/leads/read)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `leadHash` | path | `string` | yes | MD5 hash of the lead email. |
