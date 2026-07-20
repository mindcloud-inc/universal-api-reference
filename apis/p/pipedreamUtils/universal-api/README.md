# <img src="https://images.mindcloud.co/apps/icons/pipedream-utils_1776265451635.png" alt="Pipedream Utils logo" width="28" height="28"> Pipedream Utils: Universal API

Pipedream Utils provides source-available helper functions for common workflow tasks like formatting, parsing, encoding, and light data transformation.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/pipedreamUtils/latest
- **Category:** IT Operations / Integration & Automation
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://pipedream.com/apps/pipedream-utils
- **Vendor API docs:** https://raw.githubusercontent.com/PipedreamHQ/pipedream/master/components/pipedream_utils/README.md

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Formatting - [Date/Time] Add/Subtract Time](actions/add-subtract-time.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pipedreamUtils/latest/actions/add-subtract-time?connectionId=$CONNECTION_ID&inputDate=string&operation=string&duration=string&outputFormat=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Emails

| Action | Method | Description |
| --- | --- | --- |
| [Formatting - [Text] Extract Email Address](actions/extract-email-address.md) | GET | Extracts the first email address in Pipedream Utils. |

### Exchange Rates

| Action | Method | Description |
| --- | --- | --- |
| [Helper Functions - Convert Currency](actions/convert-currency.md) | GET | Converts an amount between currencies in Pipedream Utils. |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Add Files To /tmp](actions/add-files-to-tmp.md) | POST | Adds files to /tmp in Pipedream Utils. |

### Metrics

| Action | Method | Description |
| --- | --- | --- |
| [Debug Memory Usage](actions/debug-memory-usage.md) | GET | Retrieves workflow memory usage in Pipedream Utils. |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Formatting - [Date/Time] Add/Subtract Time](actions/add-subtract-time.md) | GET | Adds or subtracts time from a date in Pipedream Utils. |
| [Helper Functions - Base64 Decode String](actions/base64-decode-string.md) | GET | Decodes a Base64 string in Pipedream Utils. |
| [Helper Functions - Compare Arrays](actions/compare-arrays.md) | GET | Compares two arrays or sets in Pipedream Utils. |
| [Formatting - [Date/Time] Compare Dates](actions/compare-dates.md) | GET | Compares two dates and their duration in Pipedream Utils. |
| [Formatting - [Text] Convert HTML to Markdown](actions/convert-html-to-markdown.md) | GET | Converts HTML to Markdown in Pipedream Utils. |
| [Helper Functions - Convert HTML to Slack mrkdwn format](actions/convert-html-to-slack-mrkdwn.md) | GET | Converts HTML to Slack mrkdwn in Pipedream Utils. |
| [Formatting - [Text] Convert HTML to text](actions/convert-html-to-text.md) | GET | Converts HTML to text in Pipedream Utils. |
| [Formatting - [Data] Convert JSON to String](actions/convert-json-to-string.md) | GET | Converts JSON data to a string in Pipedream Utils. |
| [Formatting - [Text] Convert Markdown to HTML](actions/convert-markdown-to-html.md) | GET | Converts Markdown to HTML in Pipedream Utils. |
| [Helper Functions - Convert JavaScript Object to JSON String](actions/convert-object-to-json-string.md) | GET | Converts a JavaScript object to JSON in Pipedream Utils. |
| [Helper Functions - CSV File To Objects](actions/csv-file-to-objects.md) | GET | Converts a /tmp CSV file to objects in Pipedream Utils. |
| [Formatting - [Date/Time] Format](actions/date-time-format.md) | GET | Formats a date string in Pipedream Utils. |
| [Helper Functions - Export Variables](actions/export-variables.md) | GET | Exports variables for later workflow steps in Pipedream Utils. |
| [Formatting - [Text] Extract by Regular Expression](actions/extract-by-regular-expression.md) | GET | Extracts regex matches from text in Pipedream Utils. |
| [Formatting - [Text] Extract by Regular Expressions List (Regex)](actions/extract-by-regular-expressions-list.md) | GET | Extracts matches from multiple regex patterns in Pipedream Utils. |
| [Formatting - [Text] Extract Number](actions/extract-number.md) | GET | Extracts the first number in Pipedream Utils. |
| [Formatting - [Text] Extract URL](actions/extract-url.md) | GET | Extracts the first URL in Pipedream Utils. |
| [Formatting - [Numbers] Format Currency](actions/format-currency.md) | GET | Formats a number as currency in Pipedream Utils. |
| [Helper Functions - Format ISO8601 Date/Time for Google Sheets](actions/format-iso8601-datetime.md) | GET | Formats ISO 8601 values for Google Sheets in Pipedream Utils. |
| [Formatting - [Numbers] Format Number](actions/format-number.md) | GET | Formats a number without rounding in Pipedream Utils. |
| [Helper Functions - Country name, given code (2-letter)](actions/get-coutry-name-by-code-iso.md) | GET | Retrieves a country name from a two-letter code in Pipedream Utils. |
| [Helper Functions - Get Current Time in Timezone](actions/get-current-time-in-specific-timezone.md) | GET | Retrieves the current time in a timezone in Pipedream Utils. |
| [Helper Functions - Get ISO String N Days Ago](actions/get-iso-string-n-days-ago.md) | GET | Retrieves a UTC ISO timestamp from N days ago in Pipedream Utils. |
| [Helper Functions - Get Time in Timezone](actions/get-time-in-specific-timezone.md) | GET | Converts an ISO timestamp to a timezone in Pipedream Utils. |
| [Helper Functions - HTML to Markdown](actions/html-to-markdown.md) | GET | Converts HTML to Markdown with formatting options in Pipedream Utils. |

### Phone Numbers

| Action | Method | Description |
| --- | --- | --- |
| [Formatting - [Text] Extract Phone Number](actions/extract-phone-number.md) | GET | Extracts the first phone number in Pipedream Utils. |

