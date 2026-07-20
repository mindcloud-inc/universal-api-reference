# <img src="https://images.mindcloud.co/apps/icons/phrase_1774983599151.png" alt="Phrase logo" width="28" height="28"> Phrase: Universal API

Manage Phrase Strings projects, locales, keys, and translations

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/phrase/latest
- **Category:** IT Operations / Developer Tools
- **Actions:** 7
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://phrase.com
- **Vendor API docs:** https://developers.phrase.com/en/api/strings/introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Accounts](actions/list-accounts.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/phrase/latest/actions/list-accounts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (7)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Account](actions/get-account.md) | GET | Retrieves a single account from Phrase. |
| [List Accounts](actions/list-accounts.md) | GET | Retrieves a list of accounts from Phrase. |

### Key

| Action | Method | Description |
| --- | --- | --- |
| [List Keys](actions/list-keys.md) | GET | Retrieves translation keys for a project from Phrase. |

### Locale

| Action | Method | Description |
| --- | --- | --- |
| [List Locales](actions/list-locales.md) | GET | Retrieves locales for a project from Phrase. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Get Project](actions/get-project.md) | GET | Retrieves a single project from Phrase. |
| [List Projects](actions/list-projects.md) | GET | Retrieves a list of projects from Phrase. |

### Translation

| Action | Method | Description |
| --- | --- | --- |
| [List Translations](actions/list-translations.md) | GET | Retrieves translations for a project from Phrase. |

