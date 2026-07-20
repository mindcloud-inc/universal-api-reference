# Create Article with Reamaze

## Endpoint

- **Method:** `POST`
- **Path:** `/topics/:slug/articles`
- **Base URL:** `https://{brand}.reamaze.io/api/v1`
- **Official documentation:** [Create Article](https://www.reamaze.com/api/post_article)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `slug` | path | `string` | yes | Path parameter for slug. |
| `article` | body | `object` | yes | Body payload field documented on https://www.reamaze.com/api/post_article. |
