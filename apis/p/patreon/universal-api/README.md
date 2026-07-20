# <img src="https://images.mindcloud.co/apps/icons/patreon_1773266825199.png" alt="Patreon logo" width="28" height="28"> Patreon: Universal API

Manage Patreon campaigns, members, posts, and webhooks

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/patreon/latest
- **Category:** Marketing / Social Media
- **Actions:** 11
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.patreon.com
- **Vendor API docs:** https://docs.patreon.com

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Identity](actions/get-identity.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/patreon/latest/actions/get-identity?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (11)

### Announcements

| Action | Method | Description |
| --- | --- | --- |
| [Get Post](actions/get-post.md) | GET | Retrieves a post by ID from Patreon. |
| [List Posts](actions/list-posts.md) | GET | Retrieves posts for a Patreon campaign. |

### Campaigns

| Action | Method | Description |
| --- | --- | --- |
| [Get Campaign](actions/get-campaign.md) | GET | Retrieves a campaign by ID from Patreon. |
| [List Campaigns](actions/list-campaigns.md) | GET | Retrieves campaigns owned by the authorized user from Patreon. |

### Subscribers

| Action | Method | Description |
| --- | --- | --- |
| [Get Member](actions/get-member.md) | GET | Retrieves a member by ID from Patreon. |
| [List Members](actions/list-members.md) | GET | Retrieves members for a Patreon campaign. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get Identity](actions/get-identity.md) | GET | Retrieves the authenticated user's profile from Patreon. |

### Webhook Endpoints

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a webhook for the current Patreon campaign. |
| [Delete Webhook](actions/delete-webhook.md) | DELETE | Deletes an existing webhook from Patreon. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves webhooks created by your client from Patreon. |
| [Update Webhook](actions/update-webhook.md) | PUT | Updates an existing webhook in Patreon. |

