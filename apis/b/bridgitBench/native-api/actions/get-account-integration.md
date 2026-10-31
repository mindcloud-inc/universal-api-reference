# Get Account Integration with Bridgit Bench

## Endpoint

- **Method:** `GET`
- **Path:** `/rp/api/v1/accounts/:accountId/integrations`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [Get Account Integration](https://developers.gobridgit.com/reference/accountintegrations_get)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | The account ID (must be greater than zero). |
| `view` | query | `list<string>` | yes | Which slice to return: `all` (whole marketplace) or `mine` (the account's integrations and enabled products). Accepted values: `All`, `Mine`. |
| `search` | query | `string` | no | Optional free-text search over the integration name. |
| `objectTypes` | query | `list<string>` | no | Optional object-type filter (comma-delimited): people / projects / opportunities. Matches integrations exposing any of the given types. Accepted values: `Opportunities`, `People`, `Projects`. Send multiple values as a string separated by `,`. |
| `connectionStatus` | query | `list<string>` | no | Optional filter: connected / disconnected. Accepted values: `Connected`, `Disconnected`, `ReadyToConnect`. |
