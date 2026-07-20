# <img src="https://images.mindcloud.co/apps/icons/generate-bannerscom_1774878402915.png" alt="GenerateBanners.com logo" width="28" height="28"> GenerateBanners.com: Universal API

Generate banners, render images, and manage templates

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/generateBannerscom/latest
- **Category:** Marketing
- **Actions:** 4
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.generatebanners.com
- **Vendor API docs:** https://www.generatebanners.com/documentation/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Templates](actions/list-templates.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/generateBannerscom/latest/actions/list-templates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (4)

### Template

| Action | Method | Description |
| --- | --- | --- |
| [Get Template](actions/get-template.md) | GET | Retrieves metadata for one GenerateBanners.com template. |
| [Get Template Signed URL](actions/get-template-signed-url.md) | GET | Retrieves a signed render URL for a GenerateBanners.com template. |
| [List Templates](actions/list-templates.md) | GET | Retrieves metadata for all GenerateBanners.com templates. |
| [Render Template](actions/render-template.md) | GET | Retrieves a rendered image from a GenerateBanners.com template. |

