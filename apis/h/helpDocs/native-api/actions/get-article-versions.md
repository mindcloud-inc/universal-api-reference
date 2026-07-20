# Get Article Versions with HelpDocs

Retrieves article versions from HelpDocs.

## Endpoint

- **Method:** `GET`
- **Path:** `/article/:article_id/versions`
- **Base URL:** `https://api.helpdocs.io/v1`
- **Official documentation:** [Get Article Versions](https://apidocs.helpdocs.io/article/c3svl5hvb2-getting-article-versions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `article_id` | path | `string` | yes | Article ID to fetch versions for. |
| `language_code` | query | `string` | no | Language version to inspect. |
