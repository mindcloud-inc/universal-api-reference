# Add Website as Lyro Data Source [Plus plan] with Tidio

Adds a website as a Lyro data source in Tidio.

## Endpoint

- **Method:** `POST`
- **Path:** `/lyro/data-sources/website/scrape`
- **Base URL:** `https://api.tidio.com`
- **Official documentation:** [Add Website as Lyro Data Source [Plus plan]](https://developers.tidio.com/reference/post_lyro-data-sources-website-scrape)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Website URL to scrape into a Lyro data source. |
