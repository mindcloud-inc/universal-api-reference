# List Documents with SignRequest

## Endpoint

- **Method:** `GET`
- **Path:** `/documents/`
- **Base URL:** `https://signrequest.com/api/v1`
- **Official documentation:** [List Documents](https://signrequest.com/api/v1/docs/#operation/documents_list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `external_id` | query | `string` | no |
| `signrequest__who` | query | `string` | no |
| `signrequest__from_email` | query | `string` | no |
| `status` | query | `string` | no |
| `user__email` | query | `string` | no |
| `user__first_name` | query | `string` | no |
| `user__last_name` | query | `string` | no |
| `created` | query | `string` | no |
| `modified` | query | `string` | no |
