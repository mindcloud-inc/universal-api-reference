# Create Matter with DecisionVault

Creates a matter in DecisionVault and returns an invite link.

## Endpoint

- **Method:** `POST`
- **Path:** `/matters/create`
- **Base URL:** `https://api.decisionvault.com/v1`
- **Official documentation:** [Create Matter](https://docs.decisionvault.com/create-matter-21684966e0.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `context` | body | `object` | no | Optional context object with up to five string or integer key-value pairs. |
| `matter_name` | body | `string` | yes | The matter name to create in DecisionVault. |
| `questionnaire_id` | body | `string` | yes | The questionnaire ID to use when pre-creating the matter. |
