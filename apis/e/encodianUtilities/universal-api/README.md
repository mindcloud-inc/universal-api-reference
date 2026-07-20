# <img src="https://images.mindcloud.co/apps/icons/encodian_1777558985711.jpeg" alt="Encodian - Utilities logo" width="28" height="28"> Encodian - Utilities: Universal API

Use Encodian Flowr Utilities to format dates, transform text, validate values, extract data with regex, and manipulate arrays through Encodian's REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/encodianUtilities/latest
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.encodian.com/product/flowr
- **Vendor API docs:** https://support.encodian.com/hc/en-gb/articles/13253632800284-Direct-API-Integration

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Utilities - Array Add Items](actions/utilities-array-add-items.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/encodianUtilities/latest/actions/utilities-array-add-items?connectionId=$CONNECTION_ID&data=string&items=string&itemPosition=Last" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Array Add Items Result

| Action | Method | Description |
| --- | --- | --- |
| [Utilities - Array Add Items](actions/utilities-array-add-items.md) | GET |  |

### Array Contains Value Result

| Action | Method | Description |
| --- | --- | --- |
| [Utilities - Array Contains Value](actions/utilities-array-contains-value.md) | GET |  |

### Array Count

| Action | Method | Description |
| --- | --- | --- |
| [Utilities - Array Count Items](actions/utilities-array-count-items.md) | GET |  |

### Calculated Date

| Action | Method | Description |
| --- | --- | --- |
| [Utilities - Calculate Date](actions/utilities-calculate-date.md) | GET |  |

### Clean Text

| Action | Method | Description |
| --- | --- | --- |
| [Utilities - Clean Text](actions/utilities-clean-text.md) | GET |  |

### Concatenated Text

| Action | Method | Description |
| --- | --- | --- |
| [Utilities - Concatenate Text](actions/utilities-concatenate-text.md) | GET |  |

### Date Time Difference

| Action | Method | Description |
| --- | --- | --- |
| [Utilities - Get Date and Time Difference](actions/utilities-get-date-and-time-difference.md) | GET |  |

### Deduplicated Array

| Action | Method | Description |
| --- | --- | --- |
| [Utilities - Array Remove Duplicates](actions/utilities-array-remove-duplicates.md) | GET |  |

### Email Validation

| Action | Method | Description |
| --- | --- | --- |
| [Utilities - Validate Email Address](actions/utilities-validate-email-address.md) | GET |  |

### Extracted Email Addresses

| Action | Method | Description |
| --- | --- | --- |
| [Utilities - Extract Email Addresses from Text](actions/utilities-extract-email-addresses-from-text.md) | GET |  |

### Extracted Text

| Action | Method | Description |
| --- | --- | --- |
| [Utilities - Extract Text between Values](actions/utilities-extract-text-between-values.md) | GET |  |

### Extracted Urls

| Action | Method | Description |
| --- | --- | --- |
| [Utilities - Extract URLs from Text](actions/utilities-extract-urls-from-text.md) | GET |  |

### Formatted Date

| Action | Method | Description |
| --- | --- | --- |
| [Utilities - Format Date](actions/utilities-format-date.md) | GET |  |

### Formatted Text

| Action | Method | Description |
| --- | --- | --- |
| [Utilities - Format Text Case](actions/utilities-format-text-case.md) | GET |  |

### Guid

| Action | Method | Description |
| --- | --- | --- |
| [Utilities - Create GUID](actions/utilities-create-guid.md) | POST |  |

### Guid Validation

| Action | Method | Description |
| --- | --- | --- |
| [Utilities - Validate GUID](actions/utilities-validate-guid.md) | GET |  |

### Json Validation

| Action | Method | Description |
| --- | --- | --- |
| [Utilities - Validate JSON](actions/utilities-validate-json.md) | GET |  |

### Split Text Values

| Action | Method | Description |
| --- | --- | --- |
| [Utilities - Split Text](actions/utilities-split-text.md) | GET |  |

### Text Comparison

| Action | Method | Description |
| --- | --- | --- |
| [Utilities - Compare Text](actions/utilities-compare-text.md) | GET |  |

### Text Contains Value

| Action | Method | Description |
| --- | --- | --- |
| [Utilities - Text Contains Value](actions/utilities-text-contains-value.md) | GET |  |

### Text Replacement

| Action | Method | Description |
| --- | --- | --- |
| [Utilities - Replace Value with Text](actions/utilities-replace-value-with-text.md) | GET |  |

### Text Without Whitespace

| Action | Method | Description |
| --- | --- | --- |
| [Utilities - Remove Whitespace from Text](actions/utilities-remove-whitespace-from-text.md) | GET |  |

### Trimmed Text

| Action | Method | Description |
| --- | --- | --- |
| [Utilities - Trim Text](actions/utilities-trim-text.md) | GET |  |

### Url Syntax Validation

| Action | Method | Description |
| --- | --- | --- |
| [Utilities - Validate URL Syntax](actions/utilities-validate-url-syntax.md) | GET |  |

