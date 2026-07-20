# Evaluate Gate Decision with UserCheck

Requests a gate decision from UserCheck.

## Endpoint

- **Method:** `POST`
- **Path:** `/v0/gates/:gateId/decisions`
- **Base URL:** `https://api.usercheck.com`
- **Official documentation:** [Evaluate Gate Decision](https://www.usercheck.com/docs/gates/decision-endpoint)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `gate_id` | path | `string` | yes | Gate identifier from the UserCheck dashboard. |
| `email` | body | `string` | no | Email address to evaluate. Provide either Email or Domain. |
| `domain` | body | `string` | no | Domain to evaluate. Provide either Domain or Email. |
| `ip` | body | `string` | no | Optional IP address for additional intelligence. |
