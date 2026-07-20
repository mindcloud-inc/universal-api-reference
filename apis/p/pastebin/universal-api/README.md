# <img src="https://images.mindcloud.co/apps/icons/idx4b-yv7e4-logos_1777323312196.png" alt="Pastebin logo" width="28" height="28"> Pastebin: Universal API

Create, share, and manage text and code pastes

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/pastebin/latest
- **Category:** Content & Files / Storage
- **Actions:** 13
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://pastebin.com
- **Vendor API docs:** https://pastebin.com/doc_api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User Details](actions/get-current-user-details.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pastebin/latest/actions/get-current-user-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (13)

### Access Tokens

| Action | Method | Description |
| --- | --- | --- |
| [Generate User Session Key](actions/generate-user-session-key.md) | POST | Creates a Pastebin user session key. |

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [Create Guest Paste](actions/create-guest-paste.md) | POST | Creates a guest paste in Pastebin. |
| [Create Member Paste](actions/create-member-paste.md) | POST | Creates a paste in Pastebin as the current user. |
| [Create Paste In Folder](actions/create-paste-in-folder.md) | POST | Creates a paste in a Pastebin folder. |
| [Create Private Paste](actions/create-private-paste.md) | POST | Creates a private paste in Pastebin. |
| [Delete My Paste](actions/delete-my-paste.md) | DELETE | Deletes a paste created by the current Pastebin user. |
| [Get My Paste Raw Content](actions/get-my-paste-raw-content.md) | GET | Retrieves raw content for one of the user's Pastebin pastes. |
| [Get Raw Public Or Unlisted Paste](actions/get-raw-public-or-unlisted-paste.md) | GET | Retrieves raw content for a public or unlisted Pastebin paste. |
| [Get Scraped Paste Metadata](actions/get-scraped-paste-metadata.md) | GET | Retrieves metadata for a scraped Pastebin paste. |
| [Get Scraped Paste Raw Data](actions/get-scraped-paste-raw-data.md) | GET | Retrieves raw data for a scraped Pastebin paste. |
| [List My Pastes](actions/list-my-pastes.md) | GET | Retrieves pastes created by the current Pastebin user. |
| [List Recent Public Pastes](actions/list-recent-public-pastes.md) | GET | Retrieves recent public pastes from Pastebin. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User Details](actions/get-current-user-details.md) | GET | Retrieves the current Pastebin user's account details. |

