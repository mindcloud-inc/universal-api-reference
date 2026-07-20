# List Bots with QWIC

Retrieves bots from a QWIC account.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/accounts/:account_id/bots`
- **Base URL:** `https://app.qwic.ai`
- **Official documentation:** [List Bots](https://qwic-1.gitbook.io/help/building-agents/integrations/public-apis#fetch-bots-list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account_id` | path | `number` | yes | QWIC account ID from the bearer token context. |
