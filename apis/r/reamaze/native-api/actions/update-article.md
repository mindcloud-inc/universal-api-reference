# Update Article with Reamaze

## Endpoint

- **Method:** `PUT`
- **Path:** `/articles/:slug`
- **Base URL:** `https://{brand}.reamaze.io/api/v1`
- **Official documentation:** [Update Article](https://www.reamaze.com/api/put_article)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `slug` | path | `string` | yes | Path parameter for slug. |
| `article` | body | `object` | no | Body payload field documented on https://www.reamaze.com/api/put_article. |
