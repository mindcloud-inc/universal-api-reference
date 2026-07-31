# <img src="https://images.mindcloud.co/apps/icons/bacon-ipsum_1785420717434.png" alt="Bacon Ipsum logo" width="28" height="28"> Bacon Ipsum: Universal API

Generate Bacon Ipsum placeholder text as JSON paragraphs or sentences.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/baconIpsum/latest
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://baconipsum.com/
- **Vendor API docs:** https://baconipsum.com/json-api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Generate Bacon Ipsum](actions/generate-bacon-ipsum.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/baconIpsum/latest/actions/generate-bacon-ipsum?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Bacon Ipsum Text

| Action | Method | Description |
| --- | --- | --- |
| [Generate Bacon Ipsum](actions/generate-bacon-ipsum.md) | GET |  |

