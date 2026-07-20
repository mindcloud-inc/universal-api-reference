# Pipedream Utils: Native API Reference

A consolidated summary of Pipedream Utils's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://raw.githubusercontent.com/PipedreamHQ/pipedream/master/components/pipedream_utils/README.md
- **API base URL:** `https://pipedream.com`

## Authentication

### No Authentication

Pipedream Utils helper actions do not require authentication.

This API does not require request authentication.

[Official authentication documentation](https://raw.githubusercontent.com/PipedreamHQ/pipedream/master/components/pipedream_utils/README.md)

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Files To /tmp](actions/add-files-to-tmp.md) | `GET` | [docs](https://raw.githubusercontent.com/PipedreamHQ/pipedream/master/components/pipedream_utils/actions/add-files-to-tmp/add-files-to-tmp.mjs) |
| [Formatting - [Date/Time] Add/Subtract Time](actions/add-subtract-time.md) | `GET` | [docs](https://raw.githubusercontent.com/PipedreamHQ/pipedream/master/components/pipedream_utils/actions/add-subtract-time/add-subtract-time.mjs) |
| [Helper Functions - Base64 Decode String](actions/base64-decode-string.md) | `GET` | [docs](https://raw.githubusercontent.com/PipedreamHQ/pipedream/master/components/pipedream_utils/actions/base64-decode-string/base64-decode-string.mjs) |
| [Helper Functions - Compare Arrays](actions/compare-arrays.md) | `GET` | [docs](https://raw.githubusercontent.com/PipedreamHQ/pipedream/master/components/pipedream_utils/actions/compare-arrays/compare-arrays.mjs) |
| [Formatting - [Date/Time] Compare Dates](actions/compare-dates.md) | `GET` | [docs](https://raw.githubusercontent.com/PipedreamHQ/pipedream/master/components/pipedream_utils/actions/compare-dates/compare-dates.mjs) |
| [Helper Functions - Convert Currency](actions/convert-currency.md) | `GET` | [docs](https://raw.githubusercontent.com/PipedreamHQ/pipedream/master/components/pipedream_utils/actions/convert-currency/convert-currency.mjs) |
| [Formatting - [Text] Convert HTML to Markdown](actions/convert-html-to-markdown.md) | `GET` | [docs](https://raw.githubusercontent.com/PipedreamHQ/pipedream/master/components/pipedream_utils/actions/convert-html-to-markdown/convert-html-to-markdown.mjs) |
| [Helper Functions - Convert HTML to Slack mrkdwn format](actions/convert-html-to-slack-mrkdwn.md) | `GET` | [docs](https://raw.githubusercontent.com/PipedreamHQ/pipedream/master/components/pipedream_utils/actions/convert-html-to-slack-mrkdwn/convert-html-to-slack-mrkdwn.mjs) |
| [Formatting - [Text] Convert HTML to text](actions/convert-html-to-text.md) | `GET` | [docs](https://raw.githubusercontent.com/PipedreamHQ/pipedream/master/components/pipedream_utils/actions/convert-html-to-text/convert-html-to-text.mjs) |
| [Formatting - [Data] Convert JSON to String](actions/convert-json-to-string.md) | `GET` | [docs](https://raw.githubusercontent.com/PipedreamHQ/pipedream/master/components/pipedream_utils/actions/convert-json-to-string/convert-json-to-string.mjs) |
| [Formatting - [Text] Convert Markdown to HTML](actions/convert-markdown-to-html.md) | `GET` | [docs](https://raw.githubusercontent.com/PipedreamHQ/pipedream/master/components/pipedream_utils/actions/convert-markdown-to-html/convert-markdown-to-html.mjs) |
| [Helper Functions - Convert JavaScript Object to JSON String](actions/convert-object-to-json-string.md) | `GET` | [docs](https://raw.githubusercontent.com/PipedreamHQ/pipedream/master/components/pipedream_utils/actions/convert-object-to-json-string/convert-object-to-json-string.mjs) |
| [Helper Functions - CSV File To Objects](actions/csv-file-to-objects.md) | `GET` | [docs](https://raw.githubusercontent.com/PipedreamHQ/pipedream/master/components/pipedream_utils/actions/csv-file-to-objects/csv-file-to-objects.mjs) |
| [Formatting - [Date/Time] Format](actions/date-time-format.md) | `GET` | [docs](https://raw.githubusercontent.com/PipedreamHQ/pipedream/master/components/pipedream_utils/actions/date-time-format/date-time-format.mjs) |
| [Debug Memory Usage](actions/debug-memory-usage.md) | `GET` | [docs](https://raw.githubusercontent.com/PipedreamHQ/pipedream/master/components/pipedream_utils/actions/debug-memory-usage/debug-memory-usage.mjs) |
| [Helper Functions - Export Variables](actions/export-variables.md) | `GET` | [docs](https://raw.githubusercontent.com/PipedreamHQ/pipedream/master/components/pipedream_utils/actions/export-variables/export-variables.mjs) |
| [Formatting - [Text] Extract by Regular Expression](actions/extract-by-regular-expression.md) | `GET` | [docs](https://raw.githubusercontent.com/PipedreamHQ/pipedream/master/components/pipedream_utils/actions/extract-by-regular-expression/extract-by-regular-expression.mjs) |
| [Formatting - [Text] Extract by Regular Expressions List (Regex)](actions/extract-by-regular-expressions-list.md) | `GET` | [docs](https://raw.githubusercontent.com/PipedreamHQ/pipedream/master/components/pipedream_utils/actions/extract-by-regular-expressions-list/extract-by-regular-expressions-list.mjs) |
| [Formatting - [Text] Extract Email Address](actions/extract-email-address.md) | `GET` | [docs](https://raw.githubusercontent.com/PipedreamHQ/pipedream/master/components/pipedream_utils/actions/extract-email-address/extract-email-address.mjs) |
| [Formatting - [Text] Extract Number](actions/extract-number.md) | `GET` | [docs](https://raw.githubusercontent.com/PipedreamHQ/pipedream/master/components/pipedream_utils/actions/extract-number/extract-number.mjs) |
| [Formatting - [Text] Extract Phone Number](actions/extract-phone-number.md) | `GET` | [docs](https://raw.githubusercontent.com/PipedreamHQ/pipedream/master/components/pipedream_utils/actions/extract-phone-number/extract-phone-number.mjs) |
| [Formatting - [Text] Extract URL](actions/extract-url.md) | `GET` | [docs](https://raw.githubusercontent.com/PipedreamHQ/pipedream/master/components/pipedream_utils/actions/extract-url/extract-url.mjs) |
| [Formatting - [Numbers] Format Currency](actions/format-currency.md) | `GET` | [docs](https://raw.githubusercontent.com/PipedreamHQ/pipedream/master/components/pipedream_utils/actions/format-currency/format-currency.mjs) |
| [Helper Functions - Format ISO8601 Date/Time for Google Sheets](actions/format-iso8601-datetime.md) | `GET` | [docs](https://raw.githubusercontent.com/PipedreamHQ/pipedream/master/components/pipedream_utils/actions/format-iso8601-datetime/format-iso8601-datetime.mjs) |
| [Formatting - [Numbers] Format Number](actions/format-number.md) | `GET` | [docs](https://raw.githubusercontent.com/PipedreamHQ/pipedream/master/components/pipedream_utils/actions/format-number/format-number.mjs) |
| [Helper Functions - Country name, given code (2-letter)](actions/get-coutry-name-by-code-iso.md) | `GET` | [docs](https://raw.githubusercontent.com/PipedreamHQ/pipedream/master/components/pipedream_utils/actions/get-coutry-name-by-code-iso/get-coutry-name-by-code-iso.mjs) |
| [Helper Functions - Get Current Time in Timezone](actions/get-current-time-in-specific-timezone.md) | `GET` | [docs](https://raw.githubusercontent.com/PipedreamHQ/pipedream/master/components/pipedream_utils/actions/get-current-time-in-specific-timezone/get-current-time-in-specific-timezone.mjs) |
| [Helper Functions - Get ISO String N Days Ago](actions/get-iso-string-n-days-ago.md) | `GET` | [docs](https://raw.githubusercontent.com/PipedreamHQ/pipedream/master/components/pipedream_utils/actions/get-iso-string-n-days-ago/get-iso-string-n-days-ago.mjs) |
| [Helper Functions - Get Time in Timezone](actions/get-time-in-specific-timezone.md) | `GET` | [docs](https://raw.githubusercontent.com/PipedreamHQ/pipedream/master/components/pipedream_utils/actions/get-time-in-specific-timezone/get-time-in-specific-timezone.mjs) |
| [Helper Functions - HTML to Markdown](actions/html-to-markdown.md) | `GET` | [docs](https://raw.githubusercontent.com/PipedreamHQ/pipedream/master/components/pipedream_utils/actions/html-to-markdown/html-to-markdown.mjs) |
