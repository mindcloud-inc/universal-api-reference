# <img src="https://images.mindcloud.co/apps/icons/raven-tools_1775673355028.png" alt="Raven Tools logo" width="28" height="28"> Raven Tools: Universal API

Raven Tools API wrapper for campaign domains, keywords, competitors, and link-management workflows through the documented Raven API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/ravenTools/latest
- **Category:** Marketing
- **Actions:** 31
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://raventools.com
- **Vendor API docs:** https://api.raventools.com/docs/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Profile Info](actions/get-profile-info.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ravenTools/latest/actions/get-profile-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (31)

### Competitor

| Action | Method | Description |
| --- | --- | --- |
| [List Competitors](actions/list-competitors.md) | GET | Retrieves competitors for a domain in Raven Tools. |

### Domain

| Action | Method | Description |
| --- | --- | --- |
| [Add Domain](actions/add-domain.md) | POST | Creates a new domain in Raven Tools. |
| [Get Domain Info](actions/get-domain-info.md) | GET | Retrieves details for a domain in Raven Tools. |
| [List Domains](actions/list-domains.md) | GET | Retrieves domains from Raven Tools. |
| [Remove Domain](actions/remove-domain.md) | DELETE | Deletes an existing domain from Raven Tools. |

### Keyword

| Action | Method | Description |
| --- | --- | --- |
| [Add Keyword](actions/add-keyword.md) | POST | Creates a new keyword for a domain in Raven Tools. |
| [List Keywords](actions/list-keywords.md) | GET | Retrieves keywords for a domain in Raven Tools. |
| [List Keywords With Tags](actions/list-keywords-with-tags.md) | GET | Retrieves keywords and tags for a domain in Raven Tools. |
| [Remove Keyword](actions/remove-keyword.md) | DELETE | Deletes a keyword from a domain in Raven Tools. |

### Link

| Action | Method | Description |
| --- | --- | --- |
| [Activate Link](actions/activate-link.md) | PUT | Updates a link to active in Raven Tools. |
| [Create Blog Comment Link](actions/create-blog-comment-link.md) | POST | Creates a new blog comment link in Raven Tools. |
| [Create Competitor Backlink](actions/create-competitor-backlink.md) | POST | Creates a new competitor backlink in Raven Tools. |
| [Create Link](actions/create-link.md) | POST | Creates a new link in Raven Tools. |
| [Create Links](actions/create-links.md) | POST | Creates new links in Raven Tools. |
| [Create Organic Link](actions/create-organic-link.md) | POST | Creates a new organic link in Raven Tools. |
| [Create Paid Link](actions/create-paid-link.md) | POST | Creates a new paid link in Raven Tools. |
| [Create Referral Link](actions/create-referral-link.md) | POST | Creates a new referral link in Raven Tools. |
| [Deactivate Link](actions/deactivate-link.md) | PUT | Updates a link to inactive in Raven Tools. |
| [Decline Link](actions/decline-link.md) | PUT | Updates a link to declined in Raven Tools. |
| [Delete Link](actions/delete-link.md) | DELETE | Deletes an existing link from Raven Tools. |
| [Delete Links](actions/delete-links.md) | DELETE | Deletes existing links from Raven Tools. |
| [List Links](actions/list-links.md) | GET | Retrieves links for a domain in Raven Tools. |
| [List Links By Tag](actions/list-links-by-tag.md) | GET | Retrieves links by tag from Raven Tools. |
| [Queue Link](actions/queue-link.md) | POST | Creates a new queued link in Raven Tools. |
| [Request Link](actions/request-link.md) | POST | Creates a new requested link in Raven Tools. |
| [Update Link](actions/update-link.md) | PUT | Updates an existing link in Raven Tools. |
| [Update Links](actions/update-links.md) | PUT | Updates existing links in Raven Tools. |

### Link Import

| Action | Method | Description |
| --- | --- | --- |
| [Upload Links CSV](actions/upload-links-csv.md) | POST | Uploads links from a CSV file to Raven Tools. |

### Link Type

| Action | Method | Description |
| --- | --- | --- |
| [List Link Types](actions/list-link-types.md) | GET | Retrieves link types from Raven Tools. |

### Profile

| Action | Method | Description |
| --- | --- | --- |
| [Get Profile Info](actions/get-profile-info.md) | GET | Retrieves profile details from Raven Tools. |

### Website Type

| Action | Method | Description |
| --- | --- | --- |
| [List Website Types](actions/list-website-types.md) | GET | Retrieves website types from Raven Tools. |

