# <img src="https://images.mindcloud.co/apps/icons/screenshot-2026-04-23-at-22_1776994272818.png" alt="Dynamic Content Snippet logo" width="28" height="28"> Dynamic Content Snippet: Universal API

ContentSnip lets users manage URL-specific HTML snippets through a provider-hosted REST API and JavaScript snippet.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/dynamicContentSnippet/latest
- **Actions:** 2
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://contentsnip.com/
- **Vendor API docs:** https://contentsnip.com/documentation.htm

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Retrieve URL Mappings](actions/retrieve-url-mappings.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dynamicContentSnippet/latest/actions/retrieve-url-mappings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (2)

### Url Mapping

| Action | Method | Description |
| --- | --- | --- |
| [Create or Update URL Mapping](actions/create-or-update-url-mapping.md) | PUT | Updates a URL mapping in Dynamic Content Snippet, or creates one if needed. |
| [Retrieve URL Mappings](actions/retrieve-url-mappings.md) | GET | Retrieves URL mappings from Dynamic Content Snippet. |

