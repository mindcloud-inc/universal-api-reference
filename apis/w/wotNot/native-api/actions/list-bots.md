# List Bots with WotNot

Retrieves bots from WotNot.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/accounts/:account_id/bots`
- **Base URL:** `https://api.wotnot.io`
- **Official documentation:** [List Bots](https://help.wotnot.io/build/integrations/public-apis)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account_id` | path | `number` | yes | WotNot account or workspace ID. |
