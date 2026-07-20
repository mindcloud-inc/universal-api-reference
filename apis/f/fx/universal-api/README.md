# <img src="https://images.mindcloud.co/apps/icons/1001fx_1775840450244.png" alt="1001fx logo" width="28" height="28"> 1001fx: Universal API

1001fx is a function library for automation platforms, offering tested utilities for data transformation, files, images, dates, geocoding, charts, and other workflow tasks through a single API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/fx/latest
- **Category:** IT Operations / Developer Tools
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://1001fx.com
- **Vendor API docs:** https://1001fx.com/functions

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Credits](actions/get-credits.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fx/latest/actions/get-credits?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Array

| Action | Method | Description |
| --- | --- | --- |
| [Convert CSV to Array](actions/convert-csv-to-array.md) | POST | Converts a CSV file into an array of objects. |
| [Filter Array](actions/filter-array.md) | GET | Filters an array by a comparison operator. |
| [Remove Duplicates](actions/remove-duplicates.md) | GET | Removes duplicate items from an array. |

### Asset

| Action | Method | Description |
| --- | --- | --- |
| [Convert Asset to Base64](actions/convert-asset-to-base64.md) | POST | Converts an asset or URL into a base64 string. |
| [Upload Asset](actions/upload-asset.md) | POST | Uploads an asset to 1001fx and returns a temporary download URL. |

### Content

| Action | Method | Description |
| --- | --- | --- |
| [Get Content](actions/get-content.md) | GET | Retrieves structured content from a URL in 1001fx. |

### Credit

| Action | Method | Description |
| --- | --- | --- |
| [Get Credits](actions/get-credits.md) | GET | Retrieves your current 1001fx API credit balance. |

### Date Time

| Action | Method | Description |
| --- | --- | --- |
| [Format Date and Time](actions/format-date-and-time.md) | GET | Formats a date and time into a specified output format. |

### Document

| Action | Method | Description |
| --- | --- | --- |
| [Convert Office Document](actions/convert-office-document.md) | POST | Converts an office document into a PDF. |
| [Merge PDFs](actions/merge-pdfs.md) | POST | Merges up to three PDFs into one PDF. |
| [Split PDF](actions/split-pdf.md) | POST | Splits a PDF into individual pages in a ZIP file. |

### Fake Data

| Action | Method | Description |
| --- | --- | --- |
| [Create Fake Data](actions/create-fake-data.md) | POST | Creates fake test data with 1001fx. |

### Html

| Action | Method | Description |
| --- | --- | --- |
| [Scrape HTML](actions/scrape-html.md) | GET | Retrieves structured content from HTML or a website. |

### Image

| Action | Method | Description |
| --- | --- | --- |
| [Crop Image](actions/crop-image.md) | POST | Crops an image by width, height, and coordinates. |
| [Get Image Metadata](actions/get-image-metadata.md) | GET | Retrieves metadata from an image file. |
| [HTML to Image](actions/html-to-image.md) | POST | Converts HTML or a URL into an image. |
| [Resize Image](actions/resize-image.md) | POST | Resizes an image to specified dimensions. |

### Json

| Action | Method | Description |
| --- | --- | --- |
| [Get JSON Keys and Values](actions/get-json-keys-and-values.md) | GET | Retrieves JSON object keys and values. |
| [Parse String to JSON](actions/parse-string-to-json.md) | POST | Parses a string into a JSON object. |
| [Search JSON](actions/search-json.md) | GET | Finds matching key-value pairs in a JSON object. |
| [Stringify JSON](actions/stringify-json.md) | POST | Converts a JSON object into a string. |
| [Transform JSON](actions/transform-json.md) | POST | Transforms JSON into another structure using a template. |

### Qr Code

| Action | Method | Description |
| --- | --- | --- |
| [Generate QR Code](actions/generate-qr-code.md) | POST | Creates a QR code from text. |

### String

| Action | Method | Description |
| --- | --- | --- |
| [Validate String Format](actions/validate-string-format.md) | GET | Validates a string against a supported format. |

