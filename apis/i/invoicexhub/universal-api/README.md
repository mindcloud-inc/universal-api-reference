# <img src="https://images.mindcloud.co/apps/icons/invoice-api-xhub-icon_1775765856057.png" alt="Invoice.xhub logo" width="28" height="28"> Invoice.xhub: Universal API

Generate, parse, and validate electronic invoices across 14 European countries with country-specific formats such as ZUGFeRD, XRechnung, Factur-X, UBL, QR-Bill, and FatturaPA.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/invoicexhub/latest
- **Category:** Commerce / Accounting
- **Actions:** 84
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://invoice-api.xhub.io
- **Vendor API docs:** https://invoice-api.xhub.io/en/docs/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get All Supported Formats](actions/get-all-supported-formats.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/invoicexhub/latest/actions/get-all-supported-formats?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (84)

### Invoices

| Action | Method | Description |
| --- | --- | --- |
| [Auto-Detect and Parse Invoice](actions/auto-detect-and-parse-invoice.md) | GET |  |
| [Generate Austria ebInterface Invoice](actions/generate-austria-eb-interface-invoice.md) | POST |  |
| [Generate Austria PDF Invoice](actions/generate-austria-pdf-invoice.md) | POST |  |
| [Generate Belgium PDF Invoice](actions/generate-belgium-pdf-invoice.md) | POST |  |
| [Generate Belgium UBL Invoice](actions/generate-belgium-ubl-invoice.md) | POST |  |
| [Generate Bulgaria PDF Invoice](actions/generate-bulgaria-pdf-invoice.md) | POST |  |
| [Generate Bulgaria UBL Invoice](actions/generate-bulgaria-ubl-invoice.md) | POST |  |
| [Generate Czech Republic ISDOC Invoice](actions/generate-czech-republic-isdoc-invoice.md) | POST |  |
| [Generate Czech Republic PDF Invoice](actions/generate-czech-republic-pdf-invoice.md) | POST |  |
| [Generate France Factur-X Invoice](actions/generate-france-factur-x-invoice.md) | POST |  |
| [Generate France PDF Invoice](actions/generate-france-pdf-invoice.md) | POST |  |
| [Generate Germany PDF Invoice](actions/generate-germany-pdf-invoice.md) | POST |  |
| [Generate Germany XRechnung Invoice](actions/generate-germany-x-rechnung-invoice.md) | POST |  |
| [Generate Germany ZUGFeRD Invoice](actions/generate-germany-zug-fe-rd-invoice.md) | POST |  |
| [Generate Hungary NAV Invoice](actions/generate-hungary-nav-invoice.md) | POST |  |
| [Generate Hungary PDF Invoice](actions/generate-hungary-pdf-invoice.md) | POST |  |
| [Generate Italy FatturaPA Invoice](actions/generate-italy-fattura-pa-invoice.md) | POST |  |
| [Generate Italy PDF Invoice](actions/generate-italy-pdf-invoice.md) | POST |  |
| [Generate Netherlands PDF Invoice](actions/generate-netherlands-pdf-invoice.md) | POST |  |
| [Generate Netherlands UBL Invoice](actions/generate-netherlands-ubl-invoice.md) | POST |  |
| [Generate Poland PDF Invoice](actions/generate-poland-pdf-invoice.md) | POST |  |
| [Generate Portugal PDF Invoice](actions/generate-portugal-pdf-invoice.md) | POST |  |
| [Generate Romania PDF Invoice](actions/generate-romania-pdf-invoice.md) | POST |  |
| [Generate Romania UBL Invoice](actions/generate-romania-ubl-invoice.md) | POST |  |
| [Generate Spain Facturae Invoice](actions/generate-spain-facturae-invoice.md) | POST |  |
| [Generate Spain PDF Invoice](actions/generate-spain-pdf-invoice.md) | POST |  |
| [Generate Switzerland PDF Invoice](actions/generate-switzerland-pdf-invoice.md) | POST |  |
| [Generate Switzerland QR-Bill Invoice](actions/generate-switzerland-qr-bill-invoice.md) | POST |  |
| [Get All Supported Formats](actions/get-all-supported-formats.md) | GET |  |
| [Get Austria Formats](actions/get-austria-formats.md) | GET |  |
| [Get Belgium Formats](actions/get-belgium-formats.md) | GET |  |
| [Get Bulgaria Formats](actions/get-bulgaria-formats.md) | GET |  |
| [Get Czech Republic Formats](actions/get-czech-republic-formats.md) | GET |  |
| [Get France Formats](actions/get-france-formats.md) | GET |  |
| [Get Germany Formats](actions/get-germany-formats.md) | GET |  |
| [Get Hungary Formats](actions/get-hungary-formats.md) | GET |  |
| [Get Italy Formats](actions/get-italy-formats.md) | GET |  |
| [Get Netherlands Formats](actions/get-netherlands-formats.md) | GET |  |
| [Get Poland Formats](actions/get-poland-formats.md) | GET |  |
| [Get Portugal Formats](actions/get-portugal-formats.md) | GET |  |
| [Get Romania Formats](actions/get-romania-formats.md) | GET |  |
| [Get Spain Formats](actions/get-spain-formats.md) | GET |  |
| [Get Switzerland Formats](actions/get-switzerland-formats.md) | GET |  |
| [Parse Austria ebInterface Invoice](actions/parse-austria-eb-interface-invoice.md) | GET |  |
| [Parse Austria PDF Invoice](actions/parse-austria-pdf-invoice.md) | GET |  |
| [Parse Belgium PDF Invoice](actions/parse-belgium-pdf-invoice.md) | GET |  |
| [Parse Belgium UBL Invoice](actions/parse-belgium-ubl-invoice.md) | GET |  |
| [Parse Bulgaria PDF Invoice](actions/parse-bulgaria-pdf-invoice.md) | GET |  |
| [Parse Bulgaria UBL Invoice](actions/parse-bulgaria-ubl-invoice.md) | GET |  |
| [Parse Czech Republic ISDOC Invoice](actions/parse-czech-republic-isdoc-invoice.md) | GET |  |
| [Parse Czech Republic PDF Invoice](actions/parse-czech-republic-pdf-invoice.md) | GET |  |
| [Parse France Factur-X Invoice](actions/parse-france-factur-x-invoice.md) | GET |  |
| [Parse France PDF Invoice](actions/parse-france-pdf-invoice.md) | GET |  |
| [Parse Germany PDF Invoice](actions/parse-germany-pdf-invoice.md) | GET |  |
| [Parse Germany XRechnung Invoice](actions/parse-germany-x-rechnung-invoice.md) | GET |  |
| [Parse Germany ZUGFeRD Invoice](actions/parse-germany-zug-fe-rd-invoice.md) | GET |  |
| [Parse Hungary NAV Invoice](actions/parse-hungary-nav-invoice.md) | GET |  |
| [Parse Hungary PDF Invoice](actions/parse-hungary-pdf-invoice.md) | GET |  |
| [Parse Italy FatturaPA Invoice](actions/parse-italy-fattura-pa-invoice.md) | GET |  |
| [Parse Italy PDF Invoice](actions/parse-italy-pdf-invoice.md) | GET |  |
| [Parse Netherlands PDF Invoice](actions/parse-netherlands-pdf-invoice.md) | GET |  |
| [Parse Netherlands UBL Invoice](actions/parse-netherlands-ubl-invoice.md) | GET |  |
| [Parse Poland PDF Invoice](actions/parse-poland-pdf-invoice.md) | GET |  |
| [Parse Portugal PDF Invoice](actions/parse-portugal-pdf-invoice.md) | GET |  |
| [Parse Romania PDF Invoice](actions/parse-romania-pdf-invoice.md) | GET |  |
| [Parse Romania UBL Invoice](actions/parse-romania-ubl-invoice.md) | GET |  |
| [Parse Spain Facturae Invoice](actions/parse-spain-facturae-invoice.md) | GET |  |
| [Parse Spain PDF Invoice](actions/parse-spain-pdf-invoice.md) | GET |  |
| [Parse Switzerland PDF Invoice](actions/parse-switzerland-pdf-invoice.md) | GET |  |
| [Parse Switzerland QR-Bill Invoice](actions/parse-switzerland-qr-bill-invoice.md) | GET |  |
| [Validate Austria Invoice](actions/validate-austria-invoice.md) | GET |  |
| [Validate Belgium Invoice](actions/validate-belgium-invoice.md) | GET |  |
| [Validate Bulgaria Invoice](actions/validate-bulgaria-invoice.md) | GET |  |
| [Validate Czech Republic Invoice](actions/validate-czech-republic-invoice.md) | GET |  |
| [Validate France Invoice](actions/validate-france-invoice.md) | GET |  |
| [Validate Germany Invoice](actions/validate-germany-invoice.md) | GET |  |
| [Validate Hungary Invoice](actions/validate-hungary-invoice.md) | GET |  |
| [Validate Italy Invoice](actions/validate-italy-invoice.md) | GET |  |
| [Validate Netherlands Invoice](actions/validate-netherlands-invoice.md) | GET |  |
| [Validate Poland Invoice](actions/validate-poland-invoice.md) | GET |  |
| [Validate Portugal Invoice](actions/validate-portugal-invoice.md) | GET |  |
| [Validate Romania Invoice](actions/validate-romania-invoice.md) | GET |  |
| [Validate Spain Invoice](actions/validate-spain-invoice.md) | GET |  |
| [Validate Switzerland Invoice](actions/validate-switzerland-invoice.md) | GET |  |

