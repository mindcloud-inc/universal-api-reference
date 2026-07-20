# List Sites with Yeti Snow

## Endpoint

- **Method:** `GET`
- **Path:** `site/index`
- **Base URL:** `https://sandbox_api.yetisoftware.com/api/en/public_access/1715`
- **Official documentation:** [List Sites](https://documenter.getpostman.com/view/5759255/Uyxohiig)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | Page number for paginated site results. |
| `search` | query | `string` | no | Filter sites by site name. |
| `filter[archived]` | query | `boolean` | no | Include archived sites when true. |
