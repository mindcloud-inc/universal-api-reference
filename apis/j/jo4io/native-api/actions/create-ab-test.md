# Create A/B Test with jo4.io

## Endpoint

- **Method:** `POST`
- **Path:** `/protected/url/:slug/ab-test`
- **Base URL:** `https://jo4-api.jo4.io/api/v1`
- **Official documentation:** [Create A/B Test](https://jo4-api.jo4.io/swagger-ui/index.html#/ab-test-controller/createAbTest)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `slug` | path | `string` | yes |
| `splitPercentage` | body | `number` | yes |
| `variantDestination` | body | `string` | yes |
| `variantName` | body | `string` | yes |
