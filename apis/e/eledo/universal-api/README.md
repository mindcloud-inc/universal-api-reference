# <img src="https://images.mindcloud.co/apps/icons/eledo_1773954481953.png" alt="Eledo logo" width="28" height="28"> Eledo: Universal API

Generate PDFs, manage templates, and store Eledo document files

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/eledo/latest
- **Category:** Content & Files / Storage
- **Actions:** 6
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://eledo.online
- **Vendor API docs:** https://eledo.online/documentation/api_reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Profile](actions/get-profile.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eledo/latest/actions/get-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (6)

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [Generate PDF](actions/generate-pdf.md) | POST | Generates a PDF from a template in Eledo. |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Create File](actions/create-file.md) | POST | Creates a new file in Eledo. |
| [Download File](actions/download-file.md) | GET | Downloads a PDF file from Eledo. |

### Templates

| Action | Method | Description |
| --- | --- | --- |
| [Get Template Schema](actions/get-template-schema.md) | GET | Retrieves a template schema from Eledo. |
| [List Templates](actions/list-templates.md) | GET | Retrieves a list of templates from Eledo. |

### User Profiles

| Action | Method | Description |
| --- | --- | --- |
| [Get Profile](actions/get-profile.md) | GET | Retrieves the user's profile from Eledo. |

