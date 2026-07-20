# Get Order Tracking Link with AntsRoute

Retrieves an order tracking link from AntsRoute by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/capi/order/id/:id/tracking-link`
- **Base URL:** `https://app.antsroute.com`
- **Official documentation:** [Get Order Tracking Link](https://app.antsroute.com/doc-api/index.html#/Service%2FDelivery%2FCollect/getTrackingLinkById)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | — |
| `language` | query | `string` | yes | Required language enum for the tracking page. Use one of `en_GB`, `fr_FR`, `es_ES`, `de_DE`, `it_IT`, or `nl_NL`. |
