# Update Subscriber with SendMails

Updates an existing subscriber in SendMails.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/subscribers/:uid`
- **Base URL:** `https://app.sendmails.io/api/v1`
- **Official documentation:** [Update Subscriber](https://sendmails.io/docs/campaigns-apis-by-sendmails-io/#5-toc-title)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uid` | path | `string` | yes | Subscriber UID from SendMails. |
| `EMAIL` | query | `string` | yes | Subscriber email address required by SendMails update requests. |
