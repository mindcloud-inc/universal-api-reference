# Create Policy From Template with OnceOnly

Creates a policy from a template in OnceOnly.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/policies/:agent_id/from-template`
- **Base URL:** `https://api.onceonly.tech`
- **Official documentation:** [Create Policy From Template](https://docs.onceonly.tech/reference/policies/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `agent_id` | path | `string` | yes | Agent id to update policy for. |
| `template` | body | `string` | yes | Built-in template name. |
| `overrides` | body | `object` | no | Optional override object applied on top of the template. |
