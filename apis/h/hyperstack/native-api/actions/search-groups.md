# Search Groups with Hyperstack Certificates

## Endpoint

- **Method:** `POST`
- **Path:** `/groups/search`
- **Base URL:** `https://api.thehyperstack.com/v1`
- **Official documentation:** [Search Groups](https://thehyperstack.com/docs/api-guide/search-groups)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `keyword` | body | `string` | no | Search keyword matched against group titles. |
| `title` | body | `string` | no | Alias for keyword when filtering by group title. |
| `strict` | body | `boolean` | no | When true, require a contiguous phrase match. |
| `page` | body | `number` | yes | The page number for pagination. |
| `page_size` | body | `number` | yes | The number of groups to return per page. |
