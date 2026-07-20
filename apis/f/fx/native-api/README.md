# 1001fx: Native API Reference

A consolidated summary of 1001fx's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://1001fx.com/functions
- **OpenAPI specification:** https://api.1001fx.com/api-json
- **API base URL:** `https://api.1001fx.com`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://1001fx.com/functions/apikey)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Convert Asset to Base64](actions/convert-asset-to-base64.md) | `POST /files/asset2base64` | [docs](https://1001fx.com/functions/asset2base64) |
| [Convert CSV to Array](actions/convert-csv-to-array.md) | `POST /files/csv2array` | [docs](https://1001fx.com/functions/csv2array) |
| [Convert Office Document](actions/convert-office-document.md) | `POST /files/convertofficedocument` | [docs](https://1001fx.com/functions/convertofficedocument) |
| [Create Fake Data](actions/create-fake-data.md) | `POST /data/createfakedata` | [docs](https://1001fx.com/functions/createfakedata) |
| [Crop Image](actions/crop-image.md) | `POST /images/cropimage` | [docs](https://1001fx.com/functions/cropimage) |
| [Filter Array](actions/filter-array.md) | `POST /array/filterarray` | [docs](https://1001fx.com/functions/filterarray) |
| [Format Date and Time](actions/format-date-and-time.md) | `POST /datetime/formatdatetime` | [docs](https://1001fx.com/functions/formatdatetime) |
| [Generate QR Code](actions/generate-qr-code.md) | `POST /images/generateqrcode` | [docs](https://1001fx.com/functions/generateqrcode) |
| [Get Content](actions/get-content.md) | `POST /data/getcontent` | [docs](https://1001fx.com/functions/getcontent) |
| [Get Credits](actions/get-credits.md) | `POST /1001fx/getcredits` | [docs](https://1001fx.com/functions/getcredits) |
| [Get Image Metadata](actions/get-image-metadata.md) | `POST /images/getimagemeta` | [docs](https://1001fx.com/functions/getimagemeta) |
| [Get JSON Keys and Values](actions/get-json-keys-and-values.md) | `POST /data/getjsonkeysandvalues` | [docs](https://1001fx.com/functions/getjsonkeysandvalues) |
| [HTML to Image](actions/html-to-image.md) | `POST /images/html2image` | [docs](https://1001fx.com/functions/html2image) |
| [Merge PDFs](actions/merge-pdfs.md) | `POST /files/mergepdfs` | [docs](https://1001fx.com/functions/mergepdfs) |
| [Parse String to JSON](actions/parse-string-to-json.md) | `POST /data/parsestring2json` | [docs](https://1001fx.com/functions/parsestring2json) |
| [Remove Duplicates](actions/remove-duplicates.md) | `POST /array/removeduplicates` | [docs](https://1001fx.com/functions/removeduplicates) |
| [Resize Image](actions/resize-image.md) | `POST /images/resizeimage` | [docs](https://1001fx.com/functions/resizeimage) |
| [Scrape HTML](actions/scrape-html.md) | `POST /data/scrapehtml` | [docs](https://1001fx.com/functions/scrapehtml) |
| [Search JSON](actions/search-json.md) | `POST /data/deepsearchjson` | [docs](https://1001fx.com/functions/deepsearchjson) |
| [Split PDF](actions/split-pdf.md) | `POST /files/splitpdf` | [docs](https://1001fx.com/functions/splitpdf) |
| [Stringify JSON](actions/stringify-json.md) | `POST /data/stringifyjson` | [docs](https://1001fx.com/functions/stringifyjson) |
| [Transform JSON](actions/transform-json.md) | `POST /data/json2json` | [docs](https://1001fx.com/functions/json2json) |
| [Upload Asset](actions/upload-asset.md) | `POST /files/uploadasset` | [docs](https://1001fx.com/functions/uploadasset) |
| [Validate String Format](actions/validate-string-format.md) | `POST /data/validatestringformat` | [docs](https://1001fx.com/functions/validatestringformat) |
