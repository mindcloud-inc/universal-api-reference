# Get Events By NFT with OpenSea

Retrieves events for an NFT in OpenSea.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/events/chain/{chain}/contract/{address}/nfts/{identifier}`
- **Base URL:** `https://api.opensea.io`
- **Official documentation:** [Get Events By NFT](https://docs.opensea.io/reference/list_events_by_nft)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chain` | path | `string` | yes | The blockchain on which to filter the results |
| `address` | path | `string` | yes | The unique public blockchain identifier for the contract |
| `identifier` | path | `string` | yes | The NFT token id |
| `after` | query | `number` | no | Only show events after this timestamp (Unix timestamp in seconds) |
| `before` | query | `number` | no | Only show events before this timestamp (Unix timestamp in seconds) |
| `event_type[]` | query | `array<string>` | no | Filter by event types. To get order invalidation and revalidation events, please use the Stream API. The order status can also be checked on the Get Order endpoint. Send multiple values as a string separated by `,`. |
| `limit` | query | `number` | no | Number of items to return per page |
| `next.value` | query | `string` | no | — |
