# Pause Campaign with SendMails

Pauses a campaign in SendMails.

## Endpoint

- **Method:** `POST`
- **Path:** `/campaigns/:uid/pause`
- **Base URL:** `https://app.sendmails.io/api/v1`
- **Official documentation:** [Pause Campaign](https://sendmails.io/docs/campaigns-apis-by-sendmails-io/#4-toc-title)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uid` | path | `string` | yes | Campaign UID from SendMails. |
