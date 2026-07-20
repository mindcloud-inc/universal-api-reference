# Add Subscriber Tags with SendMails

Adds tags to a subscriber in SendMails.

## Endpoint

- **Method:** `POST`
- **Path:** `/subscribers/:uid/add-tag`
- **Base URL:** `https://app.sendmails.io/api/v1`
- **Official documentation:** [Add Subscriber Tags](https://sendmails.io/docs/campaigns-apis-by-sendmails-io/#5-toc-title)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tag` | query | `string` | no | One or more tag values to add, separated by commas as documented by SendMails. |
| `uid` | path | `string` | yes | Subscriber UID from SendMails. |
