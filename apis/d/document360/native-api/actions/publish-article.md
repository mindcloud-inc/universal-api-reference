# Publish Article with Document360

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/Articles/:articleId/:langCode/publish`
- **Base URL:** `https://apihub.document360.io`
- **Official documentation:** [Publish Article](https://apidocs.document360.com/apidocs/publish-an-article)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `articleId` | path | `string` | yes | The ID of the article |
| `langCode` | path | `string` | yes | The language code of the article |
| `user_id` | body | `string` | yes | The team account publishing the article |
| `version_number` | body | `number` | yes | The version to publish |
| `publish_message` | body | `string` | no | A short publish note |
