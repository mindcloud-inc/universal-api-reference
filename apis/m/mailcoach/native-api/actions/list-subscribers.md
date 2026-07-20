# List Subscribers with Mailcoach

Retrieves subscribers from a Mailcoach email list.

## Endpoint

- **Method:** `GET`
- **Path:** `/email-lists/:emailListUuid/subscribers`
- **Base URL:** `https://mindcloud.mailcoach.app/api`
- **Official documentation:** [List Subscribers](https://www.mailcoach.app/api-documentation/endpoints/subscribers/)

## Capabilities

This operation supports [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `emailListUuid` | path | `string` | yes | The UUID of the email list whose subscribers should be returned. |
| `filter[email]` | query | `string` | no | Filter subscribers by exact email address. |
| `filter[search]` | query | `string` | no | Fuzzy-search subscribers by email, name, or tags. |
| `filter[status]` | query | `string` | no | Filter subscribers by status. |
