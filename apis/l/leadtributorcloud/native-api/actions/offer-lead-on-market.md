# Offer Lead On Market with leadtributor.cloud

Creates a brokerage to offer a lead on a market in leadtributor.cloud.

## Endpoint

- **Method:** `POST`
- **Path:** `/markets/:marketId/brokerages`
- **Base URL:** `https://api.leadtributor.cloud`
- **Official documentation:** [Offer Lead On Market](https://developer.leadtributor.cloud/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `leadId` | body | `string` | yes | ID of the lead to offer on the market. |
| `marketId` | path | `string` | yes | ID of the market where the lead should be offered. |
