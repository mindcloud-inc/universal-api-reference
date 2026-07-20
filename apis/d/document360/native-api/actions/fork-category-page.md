# Fork Category Page with Document360

## Endpoint

- **Method:** `PUT`
- **Path:** `/v2/Categories/:categoryId/fork`
- **Base URL:** `https://apihub.document360.io`
- **Official documentation:** [Fork Category Page](https://apidocs.document360.com/apidocs/fork-category-page-with-an-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `categoryId` | path | `string` | yes | The ID of the category |
| `version_number` | body | `number` | yes | Category page version number to fork |
| `user_id` | body | `string` | yes | Team account ID performing the fork |
| `lang_code` | body | `string` | yes | Language code of the category page |
