# <img src="https://images.mindcloud.co/apps/icons/web-spell-checker-icon_1776344939052.png" alt="WebSpellChecker logo" width="28" height="28"> WebSpellChecker: Universal API

WebSpellChecker Cloud API for spelling, grammar, language detection, service metadata, and user-dictionary operations.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/webSpellChecker/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 18
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://webspellchecker.com
- **Vendor API docs:** https://docs.webspellchecker.com/display/WebSpellCheckerCloud/Using%2BCloud%2BWebSpellChecker%2BAPI

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Info](actions/get-info.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/webSpellChecker/latest/actions/get-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (18)

### Queries

| Action | Method | Description |
| --- | --- | --- |
| [Check Spelling](actions/check-spelling.md) | GET | Checks text for spelling errors in WebSpellChecker. |
| [Check Text](actions/check-text.md) | GET | Checks text for spelling, grammar, and style issues in WebSpellChecker. |
| [Detect Language](actions/detect-language.md) | GET | Finds likely languages for text in WebSpellChecker. |
| [Grammar Check](actions/grammar-check.md) | GET | Checks text for grammar issues in WebSpellChecker. |

### Services

| Action | Method | Description |
| --- | --- | --- |
| [Get Info](actions/get-info.md) | GET | Retrieves subscription details from WebSpellChecker. |
| [Get Language List](actions/get-language-list.md) | GET |  |
| [Get Status](actions/get-status.md) | GET | Retrieves application engine status from WebSpellChecker. |
| [Get Version](actions/get-version.md) | GET | Retrieves application version details from WebSpellChecker. |

### User Dictionary

| Action | Method | Description |
| --- | --- | --- |
| [Add User Dictionary Word](actions/add-user-dictionary-word.md) | PUT | Adds a word to a user dictionary in WebSpellChecker. |
| [Add User Dictionary Words](actions/add-user-dictionary-words.md) | PUT | Adds words to a user dictionary in WebSpellChecker. |
| [Check User Dictionary](actions/check-user-dictionary.md) | GET | Checks whether a user dictionary exists in WebSpellChecker. |
| [Create User Dictionary](actions/create-user-dictionary.md) | POST | Creates a new user dictionary in WebSpellChecker. |
| [Delete User Dictionary](actions/delete-user-dictionary.md) | DELETE | Deletes an existing user dictionary from WebSpellChecker. |
| [Delete User Dictionary Word](actions/delete-user-dictionary-word.md) | PUT | Deletes a word from a user dictionary in WebSpellChecker. |
| [Delete User Dictionary Words](actions/delete-user-dictionary-words.md) | PUT | Deletes words from a user dictionary in WebSpellChecker. |
| [Edit User Dictionary Word](actions/edit-user-dictionary-word.md) | PUT | Replaces a word in a user dictionary in WebSpellChecker. |
| [Get User Dictionary](actions/get-user-dictionary.md) | GET | Retrieves a user dictionary wordlist from WebSpellChecker. |
| [Rename User Dictionary](actions/rename-user-dictionary.md) | PUT | Renames a user dictionary in WebSpellChecker. |

