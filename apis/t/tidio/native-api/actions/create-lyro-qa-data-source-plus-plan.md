# Create Lyro QA Data Source [Plus plan] with Tidio

Creates a Lyro QA data source in Tidio.

## Endpoint

- **Method:** `POST`
- **Path:** `/lyro/data-sources/qa`
- **Base URL:** `https://api.tidio.com`
- **Official documentation:** [Create Lyro QA Data Source [Plus plan]](https://developers.tidio.com/reference/post_lyro-data-sources-qa)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | yes | Question or title for the QA data source item. |
| `content` | body | `string` | yes | Plain-text Q&A source content. |
