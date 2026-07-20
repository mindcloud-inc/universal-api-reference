# <img src="https://images.mindcloud.co/apps/icons/fina-x_1776183264192.png" alt="finaX logo" width="28" height="28"> finaX: Universal API

Finax e-invoice API for generating, converting, and rendering UBL, CII, ZUGFeRD, XRechnung, and PDF invoice artifacts.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/finaX/latest
- **Category:** Commerce / Payments & Billing
- **Actions:** 12
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor API docs:** https://docs.finax.dev/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [CII Or UBL To JSON](actions/cii-or-ubl-to-json.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/finaX/latest/actions/cii-or-ubl-to-json?connectionId=$CONNECTION_ID&file=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (12)

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [CII Invoice Xml](actions/cii-invoice-xml.md) | POST | Creates CII invoice XML from JSON in finaX. |
| [CII Or UBL To JSON](actions/cii-or-ubl-to-json.md) | GET | Retrieves invoice JSON from CII or UBL XML in finaX. |
| [CII To JSON](actions/cii-to-json.md) | GET | Retrieves invoice JSON from CII XML in finaX. |
| [Invoice XML From ZUGFeRD](actions/invoice-xml-from-zugferd.md) | GET | Retrieves invoice XML from a ZUGFeRD PDF in finaX. |
| [Merge PDF And XML](actions/merge-pdf-and-xml.md) | POST | Creates a ZUGFeRD PDF by merging PDF and XML in finaX. |
| [PDF From CII](actions/pdf-from-cii.md) | POST | Creates a ZUGFeRD PDF from CII XML in finaX. |
| [PDF From JSON](actions/pdf-from-json.md) | POST | Creates a ZUGFeRD PDF from invoice JSON in finaX. |
| [PDF From UBL](actions/pdf-from-ubl.md) | POST | Creates a ZUGFeRD PDF from UBL XML in finaX. |
| [UBL Invoice Xml](actions/ubl-invoice-xml.md) | POST | Creates UBL invoice XML from JSON in finaX. |
| [UBL To JSON](actions/ubl-to-json.md) | GET | Retrieves invoice JSON from UBL XML in finaX. |
| [XML Metadata From ZUGFeRD](actions/xml-metadata-from-zugferd.md) | GET | Retrieves XML metadata from a ZUGFeRD PDF in finaX. |
| [ZUGFeRD To JSON](actions/zugferd-to-json.md) | GET | Retrieves invoice JSON from a ZUGFeRD file in finaX. |

