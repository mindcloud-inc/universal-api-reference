# Create Subscriber with SendMails

Creates a new subscriber in SendMails.

## Endpoint

- **Method:** `POST`
- **Path:** `/subscribers`
- **Base URL:** `https://app.sendmails.io/api/v1`
- **Official documentation:** [Create Subscriber](https://sendmails.io/docs/campaigns-apis-by-sendmails-io/#5-toc-title)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `list_uid` | query | `string` | yes | List UID from SendMails. |
| `EMAIL` | query | `string` | yes | Subscriber email address. |
