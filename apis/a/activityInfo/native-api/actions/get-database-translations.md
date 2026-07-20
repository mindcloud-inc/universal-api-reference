# Get Database Translations with ActivityInfo

Retrieves ActivityInfo translations by dictionary and language.

## Endpoint

- **Method:** `GET`
- **Path:** `/resources/databases/:databaseId/dictionary/:dictionaryId/:language`
- **Base URL:** `https://www.activityinfo.org`
- **Official documentation:** [Get Database Translations](https://www.activityinfo.org/support/docs/api/reference/getTranslations.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `databaseId` | path | `string` | yes | ActivityInfo database ID. |
| `dictionaryId` | path | `string` | yes | Dictionary ID, such as database or form/{formId}. |
| `language` | path | `string` | yes | ISO two-letter language code. |
