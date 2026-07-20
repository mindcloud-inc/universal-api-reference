# Get Group with Zendesk

Retrieves a group from Zendesk.

## Endpoint

- **Method:** `GET`
- **Path:** `/groups/:group_id.json`
- **Base URL:** `https://{subdomain}.zendesk.com/api/v2`
- **Official documentation:** [Get Group](https://developer.zendesk.com/api-reference/ticketing/groups/groups/#show-group)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `group_id` | path | `number` | yes | Group ID |
