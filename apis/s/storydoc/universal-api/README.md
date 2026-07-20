# <img src="https://images.mindcloud.co/apps/icons/favicon_1774976877916.png" alt="Storydoc logo" width="28" height="28"> Storydoc: Universal API

Create, personalize, and track interactive sales stories and presentations

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/storydoc/latest
- **Category:** Marketing
- **Actions:** 4
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.storydoc.com/
- **Vendor API docs:** https://docs.storydoc.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account Details](actions/get-account-details.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/storydoc/latest/actions/get-account-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (4)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Details](actions/get-account-details.md) | GET | Retrieves account details from Storydoc. |

### Story

| Action | Method | Description |
| --- | --- | --- |
| [Get Story Details](actions/get-story-details.md) | GET | Retrieves story details from Storydoc. |
| [List Stories](actions/list-stories.md) | GET | Retrieves stories from Storydoc. |

### Version

| Action | Method | Description |
| --- | --- | --- |
| [Create Story Version](actions/create-story-version.md) | POST | Creates a new story version in Storydoc. |

