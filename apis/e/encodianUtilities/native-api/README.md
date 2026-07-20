# Encodian - Utilities: Native API Reference

A consolidated summary of Encodian - Utilities's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://support.encodian.com/hc/en-gb/articles/13253632800284-Direct-API-Integration
- **OpenAPI specification:** https://api.apps-encodian.com/swagger/Utilities/swagger.json
- **API base URL:** `https://api.apps-encodian.com`

## Authentication

### API Key

Authenticate requests to Encodian Flowr Utilities with the X-ApiKey header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-ApiKey: <apiKey>
```

[Official authentication documentation](https://support.encodian.com/hc/en-gb/articles/360012267353-Create-an-Encodian-Connection-in-Power-Automate)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Utilities - Array Add Items](actions/utilities-array-add-items.md) | `POST /api/v1/Utilities/ArrayAddItems` | [docs](https://support.encodian.com/hc/en-gb/articles/10565757970332) |
| [Utilities - Array Contains Value](actions/utilities-array-contains-value.md) | `POST /api/v1/Utilities/ArrayContainsValue` | [docs](https://support.encodian.com/hc/en-gb/articles/10242960376476) |
| [Utilities - Array Count Items](actions/utilities-array-count-items.md) | `POST /api/v1/Utilities/ArrayCountItems` | [docs](https://support.encodian.com/hc/en-gb/articles/10284117199004) |
| [Utilities - Array Remove Duplicates](actions/utilities-array-remove-duplicates.md) | `POST /api/v1/Utilities/ArrayRemoveDuplicates` | [docs](https://support.encodian.com/hc/en-gb/articles/10614334072476) |
| [Utilities - Calculate Date](actions/utilities-calculate-date.md) | `POST /api/v1/Utilities/CalculateDate` | [docs](https://support.encodian.com/hc/en-gb/articles/11311253860508) |
| [Utilities - Clean Text](actions/utilities-clean-text.md) | `POST /api/v1/Utilities/CleanString` | [docs](https://support.encodian.com/hc/en-gb/articles/10072015106077) |
| [Utilities - Compare Text](actions/utilities-compare-text.md) | `POST /api/v1/Utilities/CompareText` | [docs](https://support.encodian.com/hc/en-gb/articles/11782390540957) |
| [Utilities - Concatenate Text](actions/utilities-concatenate-text.md) | `POST /api/v1/Utilities/ConcatenateText` | [docs](https://support.encodian.com/hc/en-gb/articles/11873576674077) |
| [Utilities - Create GUID](actions/utilities-create-guid.md) | `POST /api/v1/Utilities/CreateGuid` | [docs](https://support.encodian.com/hc/en-gb/articles/9563119917597) |
| [Utilities - Extract Email Addresses from Text](actions/utilities-extract-email-addresses-from-text.md) | `POST /api/v1/Utilities/ExtractEmailAddressesFromText` | [docs](https://support.encodian.com/hc/en-gb/articles/10068475924253) |
| [Utilities - Extract Text between Values](actions/utilities-extract-text-between-values.md) | `POST /api/v1/Utilities/ExtractTextBetweenValues` | [docs](https://support.encodian.com/hc/en-gb/articles/9604938273565) |
| [Utilities - Extract URLs from Text](actions/utilities-extract-urls-from-text.md) | `POST /api/v1/Utilities/ExtractUrlsFromText` | [docs](https://support.encodian.com/hc/en-gb/articles/11056297407261) |
| [Utilities - Format Date](actions/utilities-format-date.md) | `POST /api/v1/Utilities/FormatDate` | [docs](https://support.encodian.com/hc/en-gb/articles/11053469626525) |
| [Utilities - Format Text Case](actions/utilities-format-text-case.md) | `POST /api/v1/Utilities/FormatTextCase` | [docs](https://support.encodian.com/hc/en-gb/articles/11009856518557) |
| [Utilities - Get Date and Time Difference](actions/utilities-get-date-and-time-difference.md) | `POST /api/v1/Utilities/GetDateTimeDifference` | [docs](https://support.encodian.com/hc/en-gb/articles/11753070117661) |
| [Utilities - Remove Whitespace from Text](actions/utilities-remove-whitespace-from-text.md) | `POST /api/v1/Utilities/RemoveWhitespaceFromText` | [docs](https://support.encodian.com/hc/en-gb/articles/23853140876316) |
| [Utilities - Replace Value with Text](actions/utilities-replace-value-with-text.md) | `POST /api/v1/Utilities/ReplaceValueWithText` | [docs](https://support.encodian.com/hc/en-gb/articles/11774858455709) |
| [Utilities - Split Text](actions/utilities-split-text.md) | `POST /api/v1/Utilities/SplitText` | [docs](https://support.encodian.com/hc/en-gb/articles/11846521179805) |
| [Utilities - Text Contains Value](actions/utilities-text-contains-value.md) | `POST /api/v1/Utilities/TextContainsValue` | [docs](https://support.encodian.com/hc/en-gb/articles/10515175130012/) |
| [Utilities - Trim Text](actions/utilities-trim-text.md) | `POST /api/v1/Utilities/TrimText` | [docs](https://support.encodian.com/hc/en-gb/articles/11769860640413) |
| [Utilities - Validate Email Address](actions/utilities-validate-email-address.md) | `POST /api/v1/Utilities/ValidateEmailAddress` | [docs](https://support.encodian.com/hc/en-gb/articles/9588817792925) |
| [Utilities - Validate GUID](actions/utilities-validate-guid.md) | `POST /api/v1/Utilities/ValidateGuid` | [docs](https://support.encodian.com/hc/en-gb/articles/9601440603421) |
| [Utilities - Validate JSON](actions/utilities-validate-json.md) | `POST /api/v1/Utilities/ValidateJson` | [docs](https://support.encodian.com/hc/en-gb/articles/12722049993500) |
| [Utilities - Validate URL Syntax](actions/utilities-validate-url-syntax.md) | `POST /api/v1/Utilities/ValidateUrlSyntax` | [docs](https://support.encodian.com/hc/en-gb/articles/9601816944413) |
