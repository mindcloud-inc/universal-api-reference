# Create Opportunity with ForceManager

Creates a new opportunity in ForceManager.

## Endpoint

- **Method:** `POST`
- **Path:** `/opportunities`
- **Official documentation:** [Create Opportunity](https://support.forcemanager.net/en/articles/8613478-entity-types)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `topic` | body | `string` | yes | Topic of the opportunity. |
| `probability` | body | `number` | yes | Probability of the opportunity. |
