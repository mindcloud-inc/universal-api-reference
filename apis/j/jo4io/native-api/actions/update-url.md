# Update URL with jo4.io

## Endpoint

- **Method:** `PUT`
- **Path:** `/protected/url/:id`
- **Base URL:** `https://jo4-api.jo4.io/api/v1`
- **Official documentation:** [Update URL](https://jo4-api.jo4.io/swagger-ui/index.html#/url-controller/updateUrl)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `customDomain` | body | `string` | no |
| `id` | path | `string` | yes |
| `longUrl` | body | `string` | no |
| `shortUrl` | body | `string` | no |
| `title` | body | `string` | no |
