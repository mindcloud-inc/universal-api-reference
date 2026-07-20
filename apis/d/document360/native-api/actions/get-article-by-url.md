# Get Article by URL with Document360

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/Articles`
- **Base URL:** `https://apihub.document360.io`
- **Official documentation:** [Get Article by URL](https://apidocs.document360.com/apidocs/gets-an-article-by-url)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | query | `string` | yes | The relative URL of the article without the domain |
| `redirectionMode` | query | `number` | no | How the API handles redirection |
