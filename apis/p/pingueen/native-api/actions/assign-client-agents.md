# Assign Client Agents with Pingueen

## Endpoint

- **Method:** `POST`
- **Path:** `/clients/:_id/assign-agents`
- **Base URL:** `https://api.pingueen.it/ext/v2/{businessname}`
- **Official documentation:** [Assign Client Agents](https://etinet.gitbook.io/pingueen/api-reference/clients/assign-agent-to-a-client)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `_id` | path | `string` | yes | Customer ID to assign agents to. |
| `agent` | body | `string` | yes | Agent identifier to assign. |
| `agents[]` | body | `array<object>` | yes | Agent assignments to apply. |
| `ds_notes` | body | `string` | no | Optional notes for the assignment. |
| `dt_until` | body | `date` | no | ISO 8601 expiration date for the assignment. |
