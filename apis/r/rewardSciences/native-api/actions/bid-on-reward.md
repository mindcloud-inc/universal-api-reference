# Bid On Reward with Reward Sciences

## Endpoint

- **Method:** `POST`
- **Path:** `/rewards/:rewardId/bids`
- **Base URL:** `https://api.rewardsciences.com`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `rewardId` | path | `number` | yes | The Reward Sciences reward ID. |
| `user_id` | body | `number` | yes | The user placing the bid. |
| `amount` | body | `string` | yes | Bid amount or the literal value max. |
