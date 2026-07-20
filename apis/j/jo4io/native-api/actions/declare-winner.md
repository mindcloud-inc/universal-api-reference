# Declare A/B Test Winner with jo4.io

## Endpoint

- **Method:** `POST`
- **Path:** `/protected/url/:slug/ab-test/winner/:variantId`
- **Base URL:** `https://jo4-api.jo4.io/api/v1`
- **Official documentation:** [Declare A/B Test Winner](https://jo4-api.jo4.io/swagger-ui/index.html#/ab-test-controller/declareWinner)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `slug` | path | `string` | yes |
| `variantId` | path | `string` | yes |
