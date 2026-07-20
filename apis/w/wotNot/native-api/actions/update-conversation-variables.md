# Update Conversation Variables with WotNot

Updates conversation variables in WotNot.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/accounts/:account_id/conversations/:conversation_id/variables`
- **Base URL:** `https://api.wotnot.io`
- **Official documentation:** [Update Conversation Variables](https://help.wotnot.io/build/integrations/public-apis)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account_id` | path | `number` | yes | WotNot account ID |
| `conversation_id` | path | `string` | yes | Conversation ID |
| `variables[0].name` | body | `string` | yes | Variable name |
| `variables[0].type` | body | `string` | yes | Variable scope type |
| `variables[0].value` | body | `string` | yes | Variable value |
