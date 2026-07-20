# Formatting: Native API Reference

A consolidated summary of Formatting's API configuration and 22 documented operations, with links to official documentation.

- **Official docs:** https://pipedream.com/apps/formatting
- **API base URL:** `https://postman-echo.com`

## Authentication

### No authentication

Formatting does not require credentials.

This API does not require request authentication.

[Official authentication documentation](https://pipedream.com/apps/formatting)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `content-type` | `application/json` |

## Endpoints (22 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add/Subtract Time](actions/add-subtract-time.md) | `POST /post` | [docs](https://github.com/PipedreamHQ/pipedream/blob/master/components/formatting/actions/add-subtract-time/add-subtract-time.ts) |
| [Compare Dates](actions/compare-dates.md) | `POST /post` | [docs](https://github.com/PipedreamHQ/pipedream/blob/master/components/formatting/actions/compare-dates/compare-dates.ts) |
| [Convert HTML to Markdown](actions/convert-html-to-markdown.md) | `POST /post` | [docs](https://github.com/PipedreamHQ/pipedream/blob/master/components/formatting/actions/html-to-markdown/html-to-markdown.ts) |
| [Convert HTML to Text](actions/convert-html-to-text.md) | `POST /post` | [docs](https://github.com/PipedreamHQ/pipedream/blob/master/components/formatting/actions/html-to-text/html-to-text.ts) |
| [Convert JSON to String](actions/convert-json-to-string.md) | `POST /post` | [docs](https://github.com/PipedreamHQ/pipedream/blob/master/components/formatting/actions/json-stringify/json-stringify.ts) |
| [Convert Markdown to HTML](actions/convert-markdown-to-html.md) | `POST /post` | [docs](https://github.com/PipedreamHQ/pipedream/blob/master/components/formatting/actions/markdown-to-html/markdown-to-html.ts) |
| [Date/Time Format](actions/date-time-format.md) | `POST /post` | [docs](https://github.com/PipedreamHQ/pipedream/blob/master/components/formatting/actions/date-time-format/date-time-format.ts) |
| [Decode URL](actions/decode-url.md) | `POST /post` | [docs](https://github.com/PipedreamHQ/pipedream/blob/master/components/formatting/actions/url-decode/url-decode.ts) |
| [Encode URL](actions/encode-url.md) | `POST /post` | [docs](https://github.com/PipedreamHQ/pipedream/blob/master/components/formatting/actions/url-encode/url-encode.ts) |
| [Extract by Regular Expression](actions/extract-by-regular-expression.md) | `POST /post` | [docs](https://github.com/PipedreamHQ/pipedream/blob/master/components/formatting/actions/extract-by-regex/extract-by-regex.ts) |
| [Extract Email Address](actions/extract-email-address.md) | `POST /post` | [docs](https://github.com/PipedreamHQ/pipedream/blob/master/components/formatting/actions/extract-email-address/extract-email-address.ts) |
| [Extract Number](actions/extract-number.md) | `POST /post` | [docs](https://github.com/PipedreamHQ/pipedream/blob/master/components/formatting/actions/extract-number/extract-number.ts) |
| [Extract Phone Number](actions/extract-phone-number.md) | `POST /post` | [docs](https://github.com/PipedreamHQ/pipedream/blob/master/components/formatting/actions/extract-phone-number/extract-phone-number.ts) |
| [Extract URL](actions/extract-url.md) | `POST /post` | [docs](https://github.com/PipedreamHQ/pipedream/blob/master/components/formatting/actions/extract-url/extract-url.ts) |
| [Format Currency](actions/format-currency.md) | `POST /post` | [docs](https://github.com/PipedreamHQ/pipedream/blob/master/components/formatting/actions/format-currency/format-currency.ts) |
| [Format Number](actions/format-number.md) | `POST /post` | [docs](https://github.com/PipedreamHQ/pipedream/blob/master/components/formatting/actions/format-number/format-number.ts) |
| [Parse JSON](actions/parse-json.md) | `POST /post` | [docs](https://github.com/PipedreamHQ/pipedream/blob/master/components/formatting/actions/parse-json/parse-json.ts) |
| [Replace Text](actions/replace-text.md) | `POST /post` | [docs](https://github.com/PipedreamHQ/pipedream/blob/master/components/formatting/actions/replace-text/replace-text.ts) |
| [Set Default Value](actions/set-default-value.md) | `POST /post` | [docs](https://github.com/PipedreamHQ/pipedream/blob/master/components/formatting/actions/default-value/default-value.ts) |
| [Split Text](actions/split-text.md) | `POST /post` | [docs](https://github.com/PipedreamHQ/pipedream/blob/master/components/formatting/actions/split-text/split-text.ts) |
| [Transform Case](actions/transform-case.md) | `POST /post` | [docs](https://github.com/PipedreamHQ/pipedream/blob/master/components/formatting/actions/transform-case/transform-case.ts) |
| [Trim Whitespace](actions/trim-whitespace.md) | `POST /post` | [docs](https://github.com/PipedreamHQ/pipedream/blob/master/components/formatting/actions/trim-whitespace/trim-whitespace.ts) |
