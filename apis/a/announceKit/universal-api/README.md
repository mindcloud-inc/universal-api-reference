# <img src="https://images.mindcloud.co/apps/icons/announce-kit_1777306988648.png" alt="AnnounceKit logo" width="28" height="28"> AnnounceKit: Universal API

AnnounceKit is a product communication platform for changelogs, announcements, in-app widgets, feedback, and related product updates. This connector wraps AnnounceKit's documented GraphQL API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/announceKit/latest
- **Category:** Marketing
- **Actions:** 4
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://announcekit.app
- **Vendor API docs:** https://announcekit.app/docs/graphql-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Active Project](actions/get-active-project.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/announceKit/latest/actions/get-active-project?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (4)

### Label

| Action | Method | Description |
| --- | --- | --- |
| [List Labels](actions/list-labels.md) | GET | Retrieves labels for a project in AnnounceKit. |

### Post

| Action | Method | Description |
| --- | --- | --- |
| [Create Draft Post](actions/create-draft-post.md) | POST | Creates a draft post in AnnounceKit. |
| [Publish Post](actions/publish-post.md) | POST | Creates and publishes a post in AnnounceKit. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Get Active Project](actions/get-active-project.md) | GET | Retrieves the active project from AnnounceKit. |

