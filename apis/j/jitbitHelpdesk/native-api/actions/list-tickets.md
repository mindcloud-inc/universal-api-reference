# List Tickets with Jitbit Helpdesk

## Endpoint

- **Method:** `GET`
- **Path:** `/Tickets`
- **Base URL:** `{helpdeskBaseUrl}/api`
- **Official documentation:** [List Tickets](https://www.jitbit.com/docs/api/#tickets)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mode` | body | `string` | no | Which ticket bucket to return: all, unanswered, unclosed, or handledbyme. Accepted values: `0`, `1`, `2`, `3`. |
