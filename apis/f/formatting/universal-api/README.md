# <img src="https://images.mindcloud.co/apps/icons/formatting_1776195987293.png" alt="Formatting logo" width="28" height="28"> Formatting: Universal API

Pipedream Formatting Components for transforming and parsing text, URLs, dates, numbers, JSON, HTML, and markdown.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/formatting/latest
- **Actions:** 22
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://pipedream.com/apps/formatting
- **Vendor API docs:** https://pipedream.com/apps/formatting

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Encode URL](actions/encode-url.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/formatting/latest/actions/encode-url?connectionId=$CONNECTION_ID&input=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (22)

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Add/Subtract Time](actions/add-subtract-time.md) | GET | Adds or subtracts time in the Formatting app. |
| [Compare Dates](actions/compare-dates.md) | GET | Compares two dates in the Formatting app. |
| [Convert HTML to Markdown](actions/convert-html-to-markdown.md) | GET | Converts HTML to Markdown in the Formatting app. |
| [Convert HTML to Text](actions/convert-html-to-text.md) | GET | Converts HTML to text in the Formatting app. |
| [Convert JSON to String](actions/convert-json-to-string.md) | GET | Converts JSON to a string in the Formatting app. |
| [Convert Markdown to HTML](actions/convert-markdown-to-html.md) | GET | Converts Markdown to HTML in the Formatting app. |
| [Date/Time Format](actions/date-time-format.md) | GET | Formats a date or time in the Formatting app. |
| [Decode URL](actions/decode-url.md) | GET | Decodes a URL string in the Formatting app. |
| [Extract by Regular Expression](actions/extract-by-regular-expression.md) | GET | Extracts text by regular expression in the Formatting app. |
| [Extract Email Address](actions/extract-email-address.md) | GET | Extracts an email address in the Formatting app. |
| [Extract Number](actions/extract-number.md) | GET | Extracts a number in the Formatting app. |
| [Extract Phone Number](actions/extract-phone-number.md) | GET | Extracts a phone number in the Formatting app. |
| [Extract URL](actions/extract-url.md) | GET | Extracts a URL in the Formatting app. |
| [Format Currency](actions/format-currency.md) | GET | Formats currency in the Formatting app. |
| [Format Number](actions/format-number.md) | GET | Formats a number in the Formatting app. |
| [Parse JSON](actions/parse-json.md) | GET | Parses a JSON string in the Formatting app. |
| [Replace Text](actions/replace-text.md) | GET | Replaces text in the Formatting app. |
| [Set Default Value](actions/set-default-value.md) | GET | Sets a default value in the Formatting app. |
| [Split Text](actions/split-text.md) | GET | Splits text into segments in the Formatting app. |
| [Transform Case](actions/transform-case.md) | GET | Transforms text case in the Formatting app. |
| [Trim Whitespace](actions/trim-whitespace.md) | GET | Trims whitespace from text in the Formatting app. |

### Text

| Action | Method | Description |
| --- | --- | --- |
| [Encode URL](actions/encode-url.md) | GET | Encodes a URL string in the Formatting app. |

