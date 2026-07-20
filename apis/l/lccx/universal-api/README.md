# <img src="https://images.mindcloud.co/apps/icons/lccx_1775149254734.png" alt="lc.cx logo" width="28" height="28"> lc.cx: Universal API

Create, manage, and measure short links with lc.cx

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/lccx/latest
- **Category:** Marketing
- **Actions:** 18
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://lc.cx
- **Vendor API docs:** https://dev.lc.cx

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account](actions/get-account.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lccx/latest/actions/get-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (18)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Account](actions/get-account.md) | GET | Retrieves account details from lc.cx. |

### Domain

| Action | Method | Description |
| --- | --- | --- |
| [Get Domain](actions/get-domain.md) | GET | Retrieves a branded domain from lc.cx. |
| [List Domains](actions/list-domains.md) | GET | Retrieves branded domains from lc.cx. |

### Link

| Action | Method | Description |
| --- | --- | --- |
| [Create Short Link](actions/create-short-link.md) | POST | Creates a new short link in lc.cx. |
| [Delete Link](actions/delete-link.md) | DELETE | Deletes an existing short link from lc.cx. |
| [Find Link By Path And Domain](actions/find-link-by-path-and-domain.md) | GET | Finds a short link in lc.cx by path and domain. |
| [Get Link](actions/get-link.md) | GET | Retrieves a short link from lc.cx. |
| [List Links](actions/list-links.md) | GET | Retrieves the latest short links from lc.cx. |
| [Update Link](actions/update-link.md) | PUT | Updates an existing short link in lc.cx. |

### Linkstatistics

| Action | Method | Description |
| --- | --- | --- |
| [Get Link Click Statistics](actions/get-link-click-statistics.md) | GET | Retrieves click statistics for a short link in lc.cx. |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [Create Tags](actions/create-tags.md) | POST | Creates one or more tags in lc.cx. |
| [Delete Tag](actions/delete-tag.md) | DELETE | Deletes an existing tag from lc.cx. |
| [Delete Tags in Bulk](actions/delete-tags-in-bulk.md) | DELETE | Deletes tags in bulk from lc.cx. |
| [Get Tag](actions/get-tag.md) | GET | Retrieves a tag from lc.cx. |
| [List Tags](actions/list-tags.md) | GET | Retrieves tags from lc.cx. |
| [Update Tag](actions/update-tag.md) | PUT | Updates an existing tag in lc.cx. |
| [Update Tags in Bulk](actions/update-tags-in-bulk.md) | PUT | Updates tags in bulk in lc.cx. |

### Workspace

| Action | Method | Description |
| --- | --- | --- |
| [List Workspaces](actions/list-workspaces.md) | GET | Retrieves workspaces and branded domains from lc.cx. |

