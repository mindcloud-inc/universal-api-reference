# Create Ruleset with Pinghome

Creates a new ruleset in Pinghome.

## Endpoint

- **Method:** `POST`
- **Path:** `https://incident-cmd.api.pinghome.io/v1/ruleset`
- **Base URL:** `https://api.pinghome.io`
- **Official documentation:** [Create Ruleset](https://docs.pinghome.io/incident-management/ruleset-management-and-event-handling/create-ruleset/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `rule_type` | body | `string` | yes | Type of rule to create. |
| `conditions` | body | `string<object>` | yes | JSON array of ruleset conditions. |
| `level` | body | `string` | yes | Level for the rule. |
| `team_id` | body | `string` | yes | Target team ID for the ruleset. |
| `name` | body | `string` | yes | Ruleset name. |
| `description` | body | `string` | yes | Ruleset description. |
| `urgency` | body | `string` | yes | Urgency level for generated incidents. |
| `assignees` | body | `string<object>` | no | Optional JSON array of assignee objects. |
