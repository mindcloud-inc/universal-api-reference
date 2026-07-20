# <img src="https://images.mindcloud.co/apps/icons/senja_1773697271942.png" alt="Senja logo" width="28" height="28"> Senja: Universal API

Collect, manage, and share customer testimonials

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/senja/latest
- **Category:** Marketing
- **Actions:** 3
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://senja.io
- **Vendor API docs:** https://support.senja.io/articles/rest-api-wbnz4

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Testimonials](actions/list-testimonials.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/senja/latest/actions/list-testimonials?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (3)

### Testimonial

| Action | Method | Description |
| --- | --- | --- |
| [Create Testimonial](actions/create-testimonial.md) | POST | Creates a testimonial in your Senja project. |
| [Get Testimonial](actions/get-testimonial.md) | GET | Retrieves a testimonial from Senja by ID. |
| [List Testimonials](actions/list-testimonials.md) | GET | Retrieves testimonials from your Senja project. |

