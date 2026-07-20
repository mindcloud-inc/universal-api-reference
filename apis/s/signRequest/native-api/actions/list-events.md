# List Events with SignRequest

## Endpoint

- **Method:** `GET`
- **Path:** `/events/`
- **Base URL:** `https://signrequest.com/api/v1`
- **Official documentation:** [List Events](https://signrequest.com/api/v1/docs/#operation/events_list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `document__uuid` | query | `string` | no | — |
| `document__external_id` | query | `string` | no | — |
| `document__signrequest__who` | query | `list<string>` | no | Accepted values: `m`, `mo`, `o`. |
| `document__signrequest__from_email` | query | `string` | no | — |
| `document__status` | query | `list<string>` | no | Accepted values: `ca`, `co`, `de`, `do`, `ec`, `es`, `ne`, `sd`, `se`, `si`, `vi`, `xp`. |
| `document__user__email` | query | `string` | no | — |
| `document__user__first_name` | query | `string` | no | — |
| `document__user__last_name` | query | `string` | no | — |
| `delivered` | query | `string` | no | — |
| `delivered_on` | query | `date` | no | — |
| `timestamp` | query | `date` | no | — |
| `status` | query | `list<string>` | no | Accepted values: `error`, `ok`. |
| `event_type` | query | `list<string>` | no | Accepted values: `cancelled`, `convert_error`, `converted`, `declined`, `downloaded`, `expired`, `sending_error`, `sent`, `signed`, `signer_downloaded`, `signer_email_bounced`, `signer_forwarded`, `signer_signed`, `signer_viewed`, `signer_viewed_email`, `signrequest_received`, `viewed`. |
