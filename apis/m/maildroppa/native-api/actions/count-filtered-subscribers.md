# Count Filtered Subscribers with Maildroppa

Counts Maildroppa subscribers by segment expression.

## Endpoint

- **Method:** `POST`
- **Path:** `/subscribers/filtered-count`
- **Base URL:** `https://api.maildroppa.com`
- **Official documentation:** [Count Filtered Subscribers](https://api.maildroppa.com)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filterGroups[]` | body | `array` | no | Filter groups that compose this expression. |
| `operator` | body | `string` | no | Logical operator that applies between filter groups. |
| `status` | query | `string` | no | Subscriber status filter. |
