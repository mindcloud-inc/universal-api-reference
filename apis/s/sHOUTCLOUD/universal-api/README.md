# <img src="https://images.mindcloud.co/apps/icons/shoutcloud_1785427004813.png" alt="SHOUTCLOUD logo" width="28" height="28"> SHOUTCLOUD: Universal API

Transform supplied text to uppercase using the original SHOUTCLOUD API contract.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/sHOUTCLOUD/latest
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor API docs:** https://github.com/SHOUTCLOUD/SHOUTCLOUD_NODE

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Shout Text](actions/shout-text.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sHOUTCLOUD/latest/actions/shout-text?connectionId=$CONNECTION_ID&INPUT=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Shout Result

| Action | Method | Description |
| --- | --- | --- |
| [Shout Text](actions/shout-text.md) | GET |  |

