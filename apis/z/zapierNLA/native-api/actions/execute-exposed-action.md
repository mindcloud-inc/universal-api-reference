# Execute Exposed Action with Zapier NLA

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/exposed/:exposed_app_action_id/execute/`
- **Base URL:** `https://actions.zapier.com`
- **Official documentation:** [Execute Exposed Action](https://nla.zapier.com/api/v1/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `exposed_app_action_id` | path | `string` | yes | The UUID of the exposed Zapier action to execute. |
| `instructions` | body | `string` | yes | Plain-English instructions for the exposed action. This is required by Zapier. |
| `preview_only` | body | `boolean` | no | When true, Zapier previews the action without executing it. |
