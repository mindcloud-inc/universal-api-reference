# Prepare Checkout with Eventzilla

Retrieves checkout details for an event date from Eventzilla.

## Endpoint

- **Method:** `GET`
- **Path:** `/checkout/prepare/:eventid/:dateid`
- **Base URL:** `https://www.eventzillaapi.net/api/v2`
- **Official documentation:** [Prepare Checkout](https://developer.eventzilla.net/docs/#prepare)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `eventid` | path | `number` | yes |
| `dateid` | path | `number` | yes |
