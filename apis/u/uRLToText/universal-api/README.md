# <img src="https://images.mindcloud.co/apps/icons/u-rlto-text_1778094647262.png" alt="URL to Text logo" width="28" height="28"> URL to Text: Universal API

Extract clean text, Markdown, or HTML from webpage and YouTube URLs using URLtoText.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/uRLToText/latest
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://urltotext.com/
- **Vendor API docs:** https://urltotext.com/documentation/api-docs/url-to-text/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Convert URL to Text](actions/convert-url-to-text.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uRLToText/latest/actions/convert-url-to-text?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Extracted Url Text

| Action | Method | Description |
| --- | --- | --- |
| [Convert URL to Text](actions/convert-url-to-text.md) | GET | Retrieves extracted webpage or YouTube content from URL to Text. |

