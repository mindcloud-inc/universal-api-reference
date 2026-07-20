# <img src="https://images.mindcloud.co/apps/icons/favicon-32x32_1777581886285.png" alt="PDF4me Image logo" width="28" height="28"> PDF4me Image: Universal API

Process images with PDF4me to extract metadata and text, resize, crop, compress, flip, and convert image files.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/pDF4meImage/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 2
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://dev.pdf4me.com/
- **Vendor API docs:** https://docs.pdf4me.com/power-automate/getting-started/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Image Metadata](actions/get-image-metadata.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pDF4meImage/latest/actions/get-image-metadata?connectionId=$CONNECTION_ID&docContent=string&docName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (2)

### Barcode Result

| Action | Method | Description |
| --- | --- | --- |
| [Read Barcode from Image](actions/read-barcode-from-image.md) | GET | Retrieves barcode data from an image in PDF4me Image. |

### Image File

| Action | Method | Description |
| --- | --- | --- |
| [Get Image Metadata](actions/get-image-metadata.md) | GET | Retrieves metadata for an image in PDF4me Image. |

