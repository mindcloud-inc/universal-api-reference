# <img src="https://images.mindcloud.co/apps/icons/tolq_1775828307945.png" alt="Tolq logo" width="28" height="28"> Tolq: Universal API

Tolq is a translation API for submitting text or file translation jobs, quoting work, ordering approved quotes, and retrieving completed translations.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/tolq/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 9
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.tolq.com
- **Vendor API docs:** https://docs.tolq.com/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Translation Requests](actions/list-translation-requests.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tolq/latest/actions/list-translation-requests?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (9)

### Quote Request

| Action | Method | Description |
| --- | --- | --- |
| [Create Quote Request](actions/create-quote-request.md) | POST | Creates a quote request in Tolq. |
| [Quote an Uploaded File](actions/quote-an-uploaded-file.md) | POST | Creates a quote for an uploaded file in Tolq. |

### Translation Request

| Action | Method | Description |
| --- | --- | --- |
| [Create Translation Request](actions/create-translation-request.md) | POST | Creates a translation request in Tolq. |
| [Get Translation Request](actions/get-translation-request.md) | GET | Retrieves a translation request from Tolq. |
| [List Translation Requests](actions/list-translation-requests.md) | GET | Retrieves translation requests from Tolq. |
| [Order a Quoted Request](actions/order-a-quoted-request.md) | POST | Orders a quoted translation request in Tolq. |
| [Order an Uploaded File](actions/order-an-uploaded-file.md) | POST | Orders an uploaded file in Tolq. |

### Uploaded File

| Action | Method | Description |
| --- | --- | --- |
| [Get Uploaded File Info](actions/get-uploaded-file-info.md) | GET | Retrieves uploaded file details from Tolq. |
| [Initiate File Upload](actions/initiate-file-upload.md) | POST | Initiates a file upload in Tolq. |

