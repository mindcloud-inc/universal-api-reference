# Subscribe Subscriber with SendMails

Subscribes a subscriber to a list in SendMails.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/lists/:list_uid/subscribers/:uid/subscribe`
- **Base URL:** `https://app.sendmails.io/api/v1`
- **Official documentation:** [Subscribe Subscriber](https://sendmails.io/docs/campaigns-apis-by-sendmails-io/#5-toc-title)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `list_uid` | path | `string` | yes | List UID from SendMails. |
| `uid` | path | `string` | yes | Subscriber UID from SendMails. |
