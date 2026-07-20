# <img src="https://images.mindcloud.co/apps/icons/rebrandly_1776877029641.png" alt="Rebrandly logo" width="28" height="28"> Rebrandly: Universal API

Create, manage, and analyze branded short links

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/rebrandly/latest
- **Category:** Marketing
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.rebrandly.com/
- **Vendor API docs:** https://developers.rebrandly.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account Details](actions/get-account-details.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rebrandly/latest/actions/get-account-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Details](actions/get-account-details.md) | GET | Retrieves details for the current Rebrandly account. |

### Domain

| Action | Method | Description |
| --- | --- | --- |
| [Get Domain Details](actions/get-domain-details.md) | GET | Retrieves details for a domain in Rebrandly. |
| [List Domains](actions/list-domains.md) | GET | Retrieves domains from Rebrandly. |

### Domain Count

| Action | Method | Description |
| --- | --- | --- |
| [Count Domains](actions/count-domains.md) | GET | Retrieves the number of domains in Rebrandly. |

### Link

| Action | Method | Description |
| --- | --- | --- |
| [Attach Tag To Link](actions/attach-tag-to-link.md) | PUT | Attaches a tag to a link in Rebrandly. |
| [Create Link](actions/create-link.md) | POST | Creates a new link in Rebrandly. |
| [Delete Link](actions/delete-link.md) | DELETE | Deletes an existing link from Rebrandly. |
| [Detach Tag From Link](actions/detach-tag-from-link.md) | PUT | Detaches a tag from a link in Rebrandly. |
| [Get Link Details](actions/get-link-details.md) | GET | Retrieves details for a link in Rebrandly. |
| [List Links](actions/list-links.md) | GET | Retrieves links from Rebrandly. |
| [Update Link](actions/update-link.md) | PUT | Updates an existing link in Rebrandly. |

### Link Count

| Action | Method | Description |
| --- | --- | --- |
| [Count Links](actions/count-links.md) | GET | Retrieves the number of links in Rebrandly. |

### Opengraph

| Action | Method | Description |
| --- | --- | --- |
| [Get Link OpenGraph](actions/get-link-open-graph.md) | GET | Retrieves OpenGraph metadata for a link in Rebrandly. |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Create Preset](actions/create-preset.md) | POST | Creates a preset for a template in Rebrandly. |
| [Create Query Parameter](actions/create-query-parameter.md) | POST | Creates a query parameter for a template in Rebrandly. |
| [Delete Preset](actions/delete-preset.md) | DELETE | Deletes a preset from a template in Rebrandly. |
| [Delete Query Parameter](actions/delete-query-parameter.md) | DELETE | Deletes a query parameter from a template in Rebrandly. |
| [List Presets](actions/list-presets.md) | GET | Retrieves presets for a template in Rebrandly. |
| [List Query Parameters](actions/list-query-parameters.md) | GET | Retrieves query parameters for a template in Rebrandly. |
| [Populate Preset](actions/populate-preset.md) | PUT | Populates a preset for a template in Rebrandly. |
| [Update Query Parameter](actions/update-query-parameter.md) | PUT | Updates a query parameter for a template in Rebrandly. |

### Script

| Action | Method | Description |
| --- | --- | --- |
| [List Scripts](actions/list-scripts.md) | GET | Retrieves scripts from Rebrandly. |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [Create Tag](actions/create-tag.md) | POST | Creates a new tag in Rebrandly. |
| [Delete Tag](actions/delete-tag.md) | DELETE | Deletes an existing tag from Rebrandly. |
| [Get Tag Details](actions/get-tag-details.md) | GET | Retrieves details for a tag in Rebrandly. |
| [List Tags](actions/list-tags.md) | GET | Retrieves tags from Rebrandly. |
| [Update Tag](actions/update-tag.md) | PUT | Updates an existing tag in Rebrandly. |

### Tag Count

| Action | Method | Description |
| --- | --- | --- |
| [Count Tags](actions/count-tags.md) | GET | Retrieves the number of tags in Rebrandly. |

### Template

| Action | Method | Description |
| --- | --- | --- |
| [List Templates](actions/list-templates.md) | GET | Retrieves query string templates from Rebrandly. |

### Traffic Rule

| Action | Method | Description |
| --- | --- | --- |
| [List Traffic Rules](actions/list-traffic-rules.md) | GET | Retrieves traffic rules for a link in Rebrandly. |

