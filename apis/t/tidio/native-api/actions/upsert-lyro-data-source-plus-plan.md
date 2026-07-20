# Upsert Lyro Data Source [Plus plan] with Tidio

Upserts a Lyro website data source in Tidio.

## Endpoint

- **Method:** `PUT`
- **Path:** `/lyro/data-sources/website`
- **Base URL:** `https://api.tidio.com`
- **Official documentation:** [Upsert Lyro Data Source [Plus plan]](https://developers.tidio.com/reference/put_lyro-data-sources-website)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Source URL to upsert. |
| `title` | body | `string` | yes | Title to store for the data source. |
| `content` | body | `string` | yes | HTML content to store for the data source. |
