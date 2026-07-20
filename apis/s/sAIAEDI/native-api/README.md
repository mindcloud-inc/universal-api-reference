# SAIA EDI: Native API Reference

A consolidated summary of SAIA EDI's API configuration and 5 documented operations, with links to official documentation.

- **Official docs:** https://saiaprodapi.developer.azure-api.net/api-details
- **API base URL:** `https://www.saiasecure.com`

## Authentication

### Saia API Key and Secure Login

Saia Developer Portal subscription key plus Saia Secure User ID and Password. The API key is sent as Ocp-Apim-Subscription-Key with Api-Version V1; the UserID and Password are required inside Saia XML request documents.

### Credentials

- **API Key:** `apiKey` · required
- **Saia Secure User ID:** `userId` · required · Saia Secure User ID required by Saia XML request documents.
- **Saia Secure Password:** `password` · required · Saia Secure password required by Saia XML request documents.

Send these headers with each API request:

```http
Ocp-Apim-Subscription-Key: <apiKey>
```

[Official authentication documentation](https://saiaprodapi.developer.azure-api.net/api-details)

## API conventions

Request bodies use XML.

Shared headers:

| Header | Value |
| --- | --- |
| `Api-Version` | `V1` |
| `Content-Type` | `text/xml` |

Responses from this API use XML.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (5 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Bill of Lading](actions/create-bill-of-lading.md) | `POST /webservice/BOL/xml.aspx` | [docs](https://www.saiasecure.com/webservice/bol/Create.asp) |
| [Create Pickup Request](actions/create-pickup-request.md) | `POST /webservice/pickup/xml.aspx` | [docs](https://www.saiasecure.com/webservice/pickup/Create.asp) |
| [Get Shipment by Bill of Lading Number](actions/get-shipment-by-bill-of-lading-number.md) | `POST /webservice/shipment/xml.aspx` | [docs](https://www.saiasecure.com/webservice/shipment/n_GetByBLNumber.asp) |
| [Get Shipment by PO Number](actions/get-shipment-by-po-number.md) | `POST /webservice/shipment/xml.aspx` | [docs](https://www.saiasecure.com/webservice/shipment/n_GetByPONumber.asp) |
| [Get Shipment by PRO Number](actions/get-shipment-by-pro-number.md) | `POST /webservice/shipment/xml.aspx` | [docs](https://www.saiasecure.com/webservice/shipment/n_GetByProNumber.asp) |
