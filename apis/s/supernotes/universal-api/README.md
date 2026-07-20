# <img src="https://images.mindcloud.co/apps/icons/supernotes_1776358088184.png" alt="Supernotes logo" width="28" height="28"> Supernotes: Universal API

Collaborative note-taking app built around digital notecards for ideas, records, tasks, and lists.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/supernotes/latest
- **Category:** Productivity / Knowledge Management
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://supernotes.app
- **Vendor API docs:** https://developer.supernotes.app/api-reference/introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Check Auth](actions/check-auth.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/supernotes/latest/actions/check-auth?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Access Token

| Action | Method | Description |
| --- | --- | --- |
| [Check If Fresh Access Token](actions/check-if-fresh-access-token.md) | GET | Checks whether your Supernotes access token is fresh. |

### Announcement

| Action | Method | Description |
| --- | --- | --- |
| [Get Announcements](actions/get-announcements.md) | GET |  |

### Api

| Action | Method | Description |
| --- | --- | --- |
| [Get API Version Meta](actions/get-api-version-meta.md) | GET | Retrieves version metadata from the Supernotes API. |

### Api Key

| Action | Method | Description |
| --- | --- | --- |
| [Get User API Keys](actions/get-user-api-keys.md) | GET | Retrieves your API keys from Supernotes. |

### Card

| Action | Method | Description |
| --- | --- | --- |
| [Find Card By Share Code](actions/find-card-by-share-code.md) | GET | Retrieves a Supernotes card by share code. |
| [Get Card](actions/get-card.md) | GET | Retrieves a specific card from Supernotes. |
| [Get Deleted Cards](actions/get-deleted-cards.md) | GET | Retrieves your deleted card IDs from Supernotes. |
| [Get Selected Cards](actions/get-selected-cards.md) | GET | Retrieves selected Supernotes cards using filters and ordering criteria. |

### Collection

| Action | Method | Description |
| --- | --- | --- |
| [Get Collection](actions/get-collection.md) | GET | Retrieves a specific collection from Supernotes. |
| [Get Collections](actions/get-collections.md) | GET | Retrieves your saved collections from Supernotes. |
| [Get Deleted Collections](actions/get-deleted-collections.md) | GET | Retrieves your deleted collection IDs from Supernotes. |

### Comment

| Action | Method | Description |
| --- | --- | --- |
| [Get Comments](actions/get-comments.md) | GET | Retrieves comments for a Supernotes card. |

### Credit

| Action | Method | Description |
| --- | --- | --- |
| [Get Synth Credits](actions/get-synth-credits.md) | GET | Retrieves your synthetic credits from Supernotes. |

### Email

| Action | Method | Description |
| --- | --- | --- |
| [Get Email](actions/get-email.md) | GET | Retrieves an email address from Supernotes. |
| [Get User Email Addresses](actions/get-user-email-addresses.md) | GET | Retrieves your email addresses from Supernotes. |
| [Get User Sending Email](actions/get-user-sending-email.md) | GET | Retrieves your sending email key from Supernotes. |

### Member

| Action | Method | Description |
| --- | --- | --- |
| [Get Members](actions/get-members.md) | GET | Retrieves members for a Supernotes card. |

### Pin

| Action | Method | Description |
| --- | --- | --- |
| [Get Pins](actions/get-pins.md) | GET | Retrieves your pinned cards from Supernotes. |

### Share Code

| Action | Method | Description |
| --- | --- | --- |
| [Get Share Codes For Card](actions/get-share-codes-for-card.md) | GET | Retrieves share codes for a Supernotes card. |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [Get Users Tags](actions/get-users-tags.md) | GET | Retrieves your saved tags from Supernotes. |

### Template

| Action | Method | Description |
| --- | --- | --- |
| [Get All Templates](actions/get-all-templates.md) | GET | Retrieves all of your Supernotes templates. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the authenticated user from Supernotes. |
| [Get Friends](actions/get-friends.md) | GET | Retrieves your current friends list from Supernotes. |
| [Get Incoming Requests](actions/get-incoming-requests.md) | GET | Retrieves incoming friend requests from Supernotes. |
| [Get Outgoing Requests](actions/get-outgoing-requests.md) | GET | Retrieves outgoing friend requests from Supernotes. |

### User Profile

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User Profile](actions/get-current-user-profile.md) | GET | Retrieves the authenticated user profile from Supernotes. |
| [Get Known Owner Profiles](actions/get-known-owner-profiles.md) | GET | Retrieves known card owner profiles from Supernotes. |
| [Get Other User Profile](actions/get-other-user-profile.md) | GET | Retrieves another user profile from Supernotes. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Check Auth](actions/check-auth.md) | GET | Checks your Supernotes API token and returns the user ID. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Get User Webhooks](actions/get-user-webhooks.md) | GET | Retrieves your configured webhooks from Supernotes. |

