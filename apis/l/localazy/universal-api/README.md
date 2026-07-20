# <img src="https://images.mindcloud.co/apps/icons/localazy_1782742333609.png" alt="Localazy logo" width="28" height="28"> Localazy: Universal API

Manage translation projects, files, glossary, screenshots, and AI translations

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/localazy/latest
- **Category:** IT Operations / Developer Tools
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://localazy.com
- **Vendor API docs:** https://localazy.com/docs/api/introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Projects](actions/list-projects.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/localazy/latest/actions/list-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Assets

| Action | Method | Description |
| --- | --- | --- |
| [Create Screenshot](actions/create-screenshot.md) | POST | Creates a new screenshot in a Localazy project. |
| [Delete Screenshot](actions/delete-screenshot.md) | DELETE | Deletes an existing screenshot from a Localazy project. |
| [List Screenshots](actions/list-screenshots.md) | GET | Retrieves screenshots from a Localazy project. |
| [Replace Screenshot Image](actions/replace-screenshot-image.md) | PUT | Updates an existing screenshot image in a Localazy project. |
| [Update Screenshot Metadata](actions/update-screenshot-metadata.md) | PUT | Updates screenshot tags, phrases, or metadata in Localazy. |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Delete Source Key](actions/delete-source-key.md) | DELETE | Deletes an existing source key from Localazy. |
| [Download File](actions/download-file.md) | GET | Retrieves a translated file from Localazy. |
| [List File Keys](actions/list-file-keys.md) | GET | Retrieves file keys for a project file in Localazy. |
| [List Project Files](actions/list-project-files.md) | GET | Retrieves project files from Localazy. |
| [Update Source Key](actions/update-source-key.md) | PUT | Updates an existing source key in Localazy. |

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [Import Project Content](actions/import-project-content.md) | POST | Imports localization files into a Localazy project. |
| [List Projects](actions/list-projects.md) | GET | Retrieves projects from Localazy. |
| [Translate With AI](actions/translate-with-ai.md) | POST | Creates AI translations for source strings in Localazy. |

### Releases

| Action | Method | Description |
| --- | --- | --- |
| [List CDN Metadata](actions/list-cdn-metadata.md) | GET | Retrieves CDN metadata from a Localazy project. |

### Secrets

| Action | Method | Description |
| --- | --- | --- |
| [Get Webhook Secret](actions/get-webhook-secret.md) | GET | Retrieves the webhook secret from a Localazy project. |

### Tags

| Action | Method | Description |
| --- | --- | --- |
| [List Screenshot Tags](actions/list-screenshot-tags.md) | GET | Retrieves screenshot tags from a Localazy project. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Create Glossary Term](actions/create-glossary-term.md) | POST | Creates a new glossary term in a Localazy project. |
| [Delete Glossary Term](actions/delete-glossary-term.md) | DELETE | Deletes an existing glossary term from a Localazy project. |
| [Get Glossary Term](actions/get-glossary-term.md) | GET | Retrieves a glossary term from a Localazy project. |
| [List Glossary Terms](actions/list-glossary-terms.md) | GET | Retrieves glossary terms from a Localazy project. |
| [List Import Formats](actions/list-import-formats.md) | GET | Retrieves supported import formats from Localazy. |
| [Update Glossary Term](actions/update-glossary-term.md) | PUT | Updates an existing glossary term in a Localazy project. |

### Webhook Endpoints

| Action | Method | Description |
| --- | --- | --- |
| [List Webhooks Configuration](actions/list-webhooks-configuration.md) | GET | Retrieves webhook endpoints from a Localazy project. |
| [Update Webhooks Configuration](actions/update-webhooks-configuration.md) | PUT | Updates webhook endpoints for a Localazy project. |

