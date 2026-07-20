# <img src="https://images.mindcloud.co/apps/icons/68fa36b84dda3ca442eb609c-n-fg7jw3r-bo4v-mim-wu1d-nsgy-ozu-jgzja5m-qich-ccvm-a_1781897956896.png" alt="HeadshotPro logo" width="28" height="28"> HeadshotPro: Universal API

HeadshotPro lets organizations manage team invites, teams, team members, models, headshots, favorites, and whitelabel onboarding through the HeadshotPro organization API. This draft is built from the public API docs at https://www.headshotpro.com/api and validated against a live tenant API key.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/headshotPro/latest
- **Category:** Marketing
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.headshotpro.com
- **Vendor API docs:** https://www.headshotpro.com/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Organization](actions/get-organization.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/headshotPro/latest/actions/get-organization?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Invite

| Action | Method | Description |
| --- | --- | --- |
| [Create Invite](actions/create-invite.md) | POST | Creates a new invite in HeadshotPro. |
| [Get Invite By Email](actions/get-invite-by-email.md) | GET | Finds an invite in HeadshotPro by email address. |
| [List Invites](actions/list-invites.md) | GET | Retrieves invites from HeadshotPro. |
| [Revoke Invite](actions/revoke-invite.md) | DELETE | Revokes an invite in HeadshotPro by email address. |

### Model

| Action | Method | Description |
| --- | --- | --- |
| [Create Model](actions/create-model.md) | POST | Creates a new model in HeadshotPro. |
| [Delete Model](actions/delete-model.md) | DELETE | Deletes an existing model from HeadshotPro. |
| [Get Model](actions/get-model.md) | GET | Retrieves a model from HeadshotPro. |
| [List Models](actions/list-models.md) | GET | Retrieves models from HeadshotPro. |

### Organization

| Action | Method | Description |
| --- | --- | --- |
| [Get Credits](actions/get-credits.md) | GET | Retrieves available credits from HeadshotPro. |
| [Get Organization](actions/get-organization.md) | GET | Retrieves organization details from HeadshotPro. |

### Photo

| Action | Method | Description |
| --- | --- | --- |
| [Get Favorite Model Photo](actions/get-favorite-model-photo.md) | GET | Retrieves a model's favorite photo from HeadshotPro. |
| [Get Model Photo](actions/get-model-photo.md) | GET | Retrieves a model photo from HeadshotPro. |
| [List Favorite Photos](actions/list-favorite-photos.md) | GET | Retrieves favorite photos from HeadshotPro. |
| [List Model Photos](actions/list-model-photos.md) | GET | Retrieves photos for a model in HeadshotPro. |

### Photo Download

| Action | Method | Description |
| --- | --- | --- |
| [Download Model Photos](actions/download-model-photos.md) | GET | Retrieves download URLs for model photos from HeadshotPro. |

### Team

| Action | Method | Description |
| --- | --- | --- |
| [Create Team](actions/create-team.md) | POST | Creates a new team in HeadshotPro. |
| [Delete Team](actions/delete-team.md) | DELETE | Deletes an existing team from HeadshotPro. |
| [List Teams](actions/list-teams.md) | GET | Retrieves teams from HeadshotPro. |
| [Update Team](actions/update-team.md) | PUT | Updates an existing team in HeadshotPro. |

### Team Member

| Action | Method | Description |
| --- | --- | --- |
| [Add Members To Team](actions/add-members-to-team.md) | PUT | Adds members to a team in HeadshotPro. |
| [List Accepted Team Members](actions/list-accepted-team-members.md) | GET | Retrieves accepted team members from HeadshotPro. |
| [List Finished Team Members](actions/list-finished-team-members.md) | GET | Retrieves finished team members from HeadshotPro. |
| [List Pending Team Members](actions/list-pending-team-members.md) | GET | Retrieves pending team members from HeadshotPro. |
| [List Team Members](actions/list-team-members.md) | GET | Retrieves team members from HeadshotPro. |

