# Fork Article with Document360

## Endpoint

- **Method:** `PUT`
- **Path:** `/v2/Articles/:articleId/fork`
- **Base URL:** `https://apihub.document360.io`
- **Official documentation:** [Fork Article](https://apidocs.document360.com/apidocs/fork-an-article)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `articleId` | path | `string` | yes | The ID of the article |
| `version_number` | body | `number` | yes | Version number to fork |
| `user_id` | body | `string` | yes | Team account ID performing the fork |
| `lang_code` | body | `string` | yes | Language code of the article version |
