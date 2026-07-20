# Add A/B Test Variant with jo4.io

## Endpoint

- **Method:** `POST`
- **Path:** `/protected/url/:slug/ab-test/variants`
- **Base URL:** `https://jo4-api.jo4.io/api/v1`
- **Official documentation:** [Add A/B Test Variant](https://jo4-api.jo4.io/swagger-ui/index.html#/ab-test-controller/addVariant)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `destinationUrl` | body | `string` | yes |
| `name` | body | `string` | yes |
| `percentage` | body | `number` | yes |
| `slug` | path | `string` | yes |
