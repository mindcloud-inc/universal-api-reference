# Create URL with jo4.io

## Endpoint

- **Method:** `POST`
- **Path:** `/protected/url`
- **Base URL:** `https://jo4-api.jo4.io/api/v1`
- **Official documentation:** [Create URL](https://jo4-api.jo4.io/swagger-ui/index.html#/url-controller/createUrl)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `customDomain` | body | `string` | no |
| `longUrl` | body | `string` | yes |
| `shortUrl` | body | `string` | no |
| `teamId` | body | `string` | no |
| `title` | body | `string` | no |
