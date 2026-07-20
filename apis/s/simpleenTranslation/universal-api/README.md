# <img src="https://images.mindcloud.co/apps/icons/favicon-32x32_1775159688729.png" alt="Simpleen Translation logo" width="28" height="28"> Simpleen Translation: Universal API

Translate software locale files with Simpleen's localization API and CLI.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/simpleenTranslation/latest
- **Category:** IT Operations / Developer Tools
- **Actions:** 17
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://simpleen.io/
- **Vendor API docs:** https://simpleen.io/documentation/api-reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Languages](actions/list-languages.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/simpleenTranslation/latest/actions/list-languages?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (17)

### File

| Action | Method | Description |
| --- | --- | --- |
| [Create File](actions/create-file.md) | POST | Creates a new file in Simpleen Translation. |
| [Delete File](actions/delete-file.md) | DELETE | Deletes an existing file from Simpleen Translation. |
| [Get File](actions/get-file.md) | GET | Retrieves a file from Simpleen Translation. |
| [List Files](actions/list-files.md) | GET | Retrieves files from Simpleen Translation. |
| [Update File](actions/update-file.md) | PUT | Updates an existing file in Simpleen Translation. |

### Glossary

| Action | Method | Description |
| --- | --- | --- |
| [Create Glossary](actions/create-glossary.md) | POST | Creates a new glossary in Simpleen Translation. |
| [Delete Glossary](actions/delete-glossary.md) | DELETE | Deletes an existing glossary from Simpleen Translation. |
| [Get Glossary](actions/get-glossary.md) | GET | Retrieves a glossary from Simpleen Translation. |
| [List Glossaries](actions/list-glossaries.md) | GET | Retrieves glossaries from Simpleen Translation. |
| [Update Glossary](actions/update-glossary.md) | PUT | Updates an existing glossary in Simpleen Translation. |

### Language

| Action | Method | Description |
| --- | --- | --- |
| [Get Language](actions/get-language.md) | GET | Retrieves a language from Simpleen Translation. |
| [List Languages](actions/list-languages.md) | GET | Retrieves languages from Simpleen Translation. |

### Segment

| Action | Method | Description |
| --- | --- | --- |
| [Create Segment](actions/create-segment.md) | POST | Creates a new segment in Simpleen Translation. |
| [Delete Segment](actions/delete-segment.md) | DELETE | Deletes an existing segment from Simpleen Translation. |
| [Get Segment](actions/get-segment.md) | GET | Retrieves a segment from Simpleen Translation. |
| [List Segments](actions/list-segments.md) | GET | Retrieves segments from Simpleen Translation. |
| [Update Segment](actions/update-segment.md) | PUT | Updates an existing segment in Simpleen Translation. |

