# <img src="https://images.mindcloud.co/apps/icons/lnk-bio_1774529800984.png" alt="Lnk.Bio logo" width="28" height="28"> Lnk.Bio: Universal API

Manage your Lnk.Bio profile, Lnks, and groups through the official Lnk.Bio API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/lnkBio/latest
- **Category:** Marketing
- **Actions:** 5
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://lnk.bio/
- **Vendor API docs:** https://api.lnk.bio/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Retrieve Basic Profile Info](actions/retrieve-basic-profile-info.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lnkBio/latest/actions/retrieve-basic-profile-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (5)

### Group

| Action | Method | Description |
| --- | --- | --- |
| [List Lnk Groups](actions/list-lnk-groups.md) | GET | Retrieves Lnk groups from Lnk.Bio. |

### Lnk

| Action | Method | Description |
| --- | --- | --- |
| [Create Lnk](actions/create-lnk.md) | POST | Creates a new Lnk in Lnk.Bio. |
| [Delete Lnk](actions/delete-lnk.md) | DELETE | Deletes an existing Lnk from Lnk.Bio. |
| [List Lnks](actions/list-lnks.md) | GET | Retrieves current Lnks from Lnk.Bio. |

### Profile

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Basic Profile Info](actions/retrieve-basic-profile-info.md) | GET | Retrieves the authenticated user's profile from Lnk.Bio. |

