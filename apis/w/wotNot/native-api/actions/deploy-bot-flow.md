# Deploy Bot Flow with WotNot

Deploys a bot flow in WotNot.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/bots/:bot_id/deploy`
- **Base URL:** `https://api.wotnot.io`
- **Official documentation:** [Deploy Bot Flow](https://help.wotnot.io/build/integrations/public-apis)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bot_id` | path | `number` | yes | WotNot bot ID |
| `flow_diagram` | body | `string` | yes | Bot flow JSON to deploy |
