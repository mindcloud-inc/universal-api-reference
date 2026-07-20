# Delete Alert Rules with Umbrella

Deletes existing alert rules from Umbrella.

## Endpoint

- **Method:** `DELETE`
- **Path:** `https://api.sse.cisco.com/admin/v2/alerting/rules`
- **Base URL:** `https://api.umbrella.com`
- **Official documentation:** [Delete Alert Rules](https://developer.cisco.com/docs/cloud-security/delete-alert-rules/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ruleIds` | body | `list<number>` | yes | A list of alert rule IDs to delete. |
