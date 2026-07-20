# List Matters with DecisionVault

Retrieves matters from your firm in DecisionVault.

## Endpoint

- **Method:** `GET`
- **Path:** `/matters`
- **Base URL:** `https://api.decisionvault.com/v1`
- **Official documentation:** [List Matters](https://docs.decisionvault.com/get-matters-21684961e0.md)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | query | `date` | no | Filter matters created from this date, inclusive. |
| `is_submitted` | query | `number` | no | Filter matters by submit status: 1 for submitted or 0 for not submitted. |
| `quest_approach` | query | `string` | no | Filter matters by questionnaire approach or type. |
| `search` | query | `string` | no | Only return matters whose name contains this search term (case-insensitive). |
| `until` | query | `date` | no | Filter matters created until this date, inclusive. |
