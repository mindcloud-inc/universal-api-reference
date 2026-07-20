# Search Articles by Translation Status with Document360

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/Translations/:projectVersionId/:langCode`
- **Base URL:** `https://apihub.document360.io`
- **Official documentation:** [Search Articles by Translation Status](https://apidocs.document360.com/apidocs/gets-article-to-be-translated)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectVersionId` | path | `string` | yes | The ID of the version |
| `langCode` | path | `string` | yes | The language code of the version |
| `status` | query | `number` | no | Translation status filter |
