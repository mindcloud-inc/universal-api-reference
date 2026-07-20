# <img src="https://images.mindcloud.co/apps/icons/imagior_1775051110437.png" alt="Imagior logo" width="28" height="28"> Imagior: Universal API

Generate images and inspect templates with Imagior

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/imagior/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 5
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://imagior.com
- **Vendor API docs:** https://docs.imagior.com

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Retrieve Account Details](actions/retrieve-account-details.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/imagior/latest/actions/retrieve-account-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (5)

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Generate Image](actions/generate-image.md) | POST | Creates an image in Imagior from a template. |

### Templates

| Action | Method | Description |
| --- | --- | --- |
| [List All Templates](actions/list-all-templates.md) | GET | Retrieves templates from Imagior. |
| [List Template Elements](actions/list-template-elements.md) | GET | Retrieves template elements from Imagior. |
| [List Template Elements and Their Basic Properties](actions/list-template-elements-and-their-basic-properties.md) | GET | Retrieves basic template element properties from Imagior. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Account Details](actions/retrieve-account-details.md) | GET | Retrieves account details from Imagior. |

