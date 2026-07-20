# <img src="https://images.mindcloud.co/apps/icons/tender-support_1775666481743.jpeg" alt="Tender Support logo" width="28" height="28"> Tender Support: Universal API

Tender Support is a support forum and knowledge-base platform. This app connects to Tender's JSON REST API for managing site discussions, users, queues, categories, companies, and knowledge-base content on the configured Tender support site.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/tenderSupport/latest
- **Category:** Support / Ticketing
- **Actions:** 10
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://tenderapp.com
- **Vendor API docs:** https://help.tenderapp.com/kb/api/introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Site](actions/get-site.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tenderSupport/latest/actions/get-site?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (10)

### Categories

| Action | Method | Description |
| --- | --- | --- |
| [Get Category](actions/get-category.md) | GET | Retrieves a category from Tender Support. |
| [List Categories](actions/list-categories.md) | GET | Retrieves support categories from Tender Support. |

### Tickets

| Action | Method | Description |
| --- | --- | --- |
| [Get Discussion](actions/get-discussion.md) | GET | Retrieves a discussion from Tender Support. |
| [List Discussions](actions/list-discussions.md) | GET | Retrieves support discussions from Tender Support. |
| [List Queue Discussions](actions/list-queue-discussions.md) | GET | Retrieves discussions from a Tender Support queue. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Get Article](actions/get-article.md) | GET | Retrieves a knowledge base article from Tender Support. |
| [Get Site](actions/get-site.md) | GET | Retrieves site details from Tender Support. |
| [List Articles](actions/list-articles.md) | GET | Retrieves knowledge base articles from Tender Support. |
| [List Sections](actions/list-sections.md) | GET | Retrieves support sections from Tender Support. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Create User](actions/create-user.md) | POST | Creates a new user in Tender Support. |

