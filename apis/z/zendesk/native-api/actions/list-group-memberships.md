# List Group Memberships with Zendesk

Retrieves a list of group memberships from Zendesk.

## Endpoint

- **Method:** `GET`
- **Path:** `/group_memberships.json`
- **Base URL:** `https://{subdomain}.zendesk.com/api/v2`
- **Official documentation:** [List Group Memberships](https://developer.zendesk.com/api-reference/ticketing/groups/group_memberships/#list-memberships)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user_id` | query | `number` | no | Filter memberships by user ID. |
| `group_id` | query | `number` | no | Filter memberships by group ID. |
