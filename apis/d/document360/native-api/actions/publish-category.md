# Publish Category with Document360

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/Categories/:categoryId/:langCode/publish`
- **Base URL:** `https://apihub.document360.io`
- **Official documentation:** [Publish Category](https://apidocs.document360.com/apidocs/publishes-an-category-with-an-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `categoryId` | path | `string` | yes | The ID of the category |
| `langCode` | path | `string` | yes | Language code of the category |
| `user_id` | body | `string` | yes | Team account ID responsible for the publish |
| `version_number` | body | `number` | yes | Category version number to publish |
| `publish_message` | body | `string` | no | Optional publish message |
