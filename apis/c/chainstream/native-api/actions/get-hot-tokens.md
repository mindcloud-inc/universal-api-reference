# Get Hot Tokens with Chainstream

Retrieves hot tokens from Chainstream.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/ranking/:chain/hotTokens/:duration`
- **Base URL:** `https://api.chainstream.io`
- **Official documentation:** [Get Hot Tokens](https://docs.chainstream.io/en/api-reference/endpoint/data/ranking/v2/ranking-chain-hottokens-duration-get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chain` | path | `string` | yes | A chain name listed in supported networks. |
| `duration` | path | `string` | yes | Duration of the ranking. |
| `sortBy` | query | `string` | no | Sort field. |
| `sortDirection` | query | `string` | no | Sort direction. |
| `tag` | query | `string` | no | Ranking tag filter. |
| `searchKeywords[]` | query | `array<string>` | no | Search keywords. |
| `excludeKeywords[]` | query | `array<string>` | no | Exclude keywords. |
