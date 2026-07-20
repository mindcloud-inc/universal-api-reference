# <img src="https://images.mindcloud.co/apps/icons/real-favicon-generator_1777482221448.png" alt="RealFaviconGenerator logo" width="28" height="28"> RealFaviconGenerator: Universal API

RealFaviconGenerator creates favicon packages, HTML markup, and update metadata for browser and platform favicon support.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/realFaviconGenerator/latest
- **Actions:** 3
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://realfavicongenerator.net/
- **Vendor API docs:** https://realfavicongenerator.net/developers

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List change log](actions/list-change-log.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/realFaviconGenerator/latest/actions/list-change-log?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (3)

### Change Log Entry

| Action | Method | Description |
| --- | --- | --- |
| [List change log](actions/list-change-log.md) | GET |  |

### Favicon Generation Session

| Action | Method | Description |
| --- | --- | --- |
| [Start favicon generation](actions/start-favicon-generation.md) | POST |  |

### Version

| Action | Method | Description |
| --- | --- | --- |
| [List versions](actions/list-versions.md) | GET |  |

