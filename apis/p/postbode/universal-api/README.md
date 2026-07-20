# <img src="https://images.mindcloud.co/apps/icons/favicon-www-postbode-nu-48x48_1776783272759.png" alt="Postbode logo" width="28" height="28"> Postbode: Universal API

Manage Postbode mailboxes and send physical letters

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/postbode/latest
- **Actions:** 5
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.postbode.nu
- **Vendor API docs:** https://api.postbode.nu

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Mailboxes](actions/list-mailboxes.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/postbode/latest/actions/list-mailboxes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (5)

### Letter

| Action | Method | Description |
| --- | --- | --- |
| [Create Letter Draft](actions/create-letter-draft.md) | POST | Creates a draft letter in a Postbode mailbox. |
| [Get Letter](actions/get-letter.md) | GET | Retrieves a letter from a specific Postbode mailbox. |
| [List Letters](actions/list-letters.md) | GET | Retrieves letters from a specific Postbode mailbox. |
| [Send Letter](actions/send-letter.md) | POST | Creates and sends a letter from a Postbode mailbox. |

### Mailbox

| Action | Method | Description |
| --- | --- | --- |
| [List Mailboxes](actions/list-mailboxes.md) | GET | Retrieves available mailboxes from the Postbode API. |

