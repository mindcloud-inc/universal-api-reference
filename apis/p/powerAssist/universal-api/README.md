# <img src="https://images.mindcloud.co/apps/icons/power-assist-icon_1778173392378.png" alt="Power Assist logo" width="28" height="28"> Power Assist: Universal API

Power Assist provides utility and data-manipulation actions for arrays, strings, math, type checks, and validation through Elevate Digital's RapidAPI-backed API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/powerAssist/latest
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://elevate-digital.com/powerassist/
- **Vendor API docs:** https://learn.microsoft.com/en-us/connectors/powerassist/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Clean Whitespace](actions/clean-whitespace.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/powerAssist/latest/actions/clean-whitespace?connectionId=$CONNECTION_ID&string=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Any Match Result

| Action | Method | Description |
| --- | --- | --- |
| [Check Any Array Item](actions/check-any-array-item.md) | GET | Checks whether any array item matches in Power Assist. |

### Array After Removal

| Action | Method | Description |
| --- | --- | --- |
| [Remove First Array Item](actions/remove-first-array-item.md) | GET | Removes the first matching array item with Power Assist. |

### Average Result

| Action | Method | Description |
| --- | --- | --- |
| [Calculate Average](actions/calculate-average.md) | GET | Calculates an average with Power Assist. |

### Cleaned String

| Action | Method | Description |
| --- | --- | --- |
| [Clean Whitespace](actions/clean-whitespace.md) | GET | Cleans whitespace in a string with Power Assist. |

### Email Validation Result

| Action | Method | Description |
| --- | --- | --- |
| [Validate Email](actions/validate-email.md) | GET | Validates an email address with Power Assist. |

### Escaped Html

| Action | Method | Description |
| --- | --- | --- |
| [Escape HTML](actions/escape-html.md) | GET | Escapes HTML characters with Power Assist. |

### Every Match Result

| Action | Method | Description |
| --- | --- | --- |
| [Check Every Array Item](actions/check-every-array-item.md) | GET | Checks whether every array item matches in Power Assist. |

### Filtered Array

| Action | Method | Description |
| --- | --- | --- |
| [Filter Array](actions/filter-array.md) | GET | Filters an array with Power Assist. |

### First Matching Item

| Action | Method | Description |
| --- | --- | --- |
| [Find First Array Item](actions/find-first-array-item.md) | GET | Finds the first matching array item with Power Assist. |

### Grouped Array

| Action | Method | Description |
| --- | --- | --- |
| [Group Array By Property](actions/group-array-by-property.md) | GET | Groups an array by property with Power Assist. |

### Median Result

| Action | Method | Description |
| --- | --- | --- |
| [Calculate Median](actions/calculate-median.md) | GET | Calculates a median with Power Assist. |

### Plain Text

| Action | Method | Description |
| --- | --- | --- |
| [Strip HTML](actions/strip-html.md) | GET | Strips HTML from a string with Power Assist. |

### Prepended Array

| Action | Method | Description |
| --- | --- | --- |
| [Prepend To Array](actions/prepend-to-array.md) | GET | Prepends a value to an array with Power Assist. |

### Regex Replacement Result

| Action | Method | Description |
| --- | --- | --- |
| [Replace Text With Regex](actions/replace-text-with-regex.md) | GET | Replaces text by regex in Power Assist. |

### Replacement Result

| Action | Method | Description |
| --- | --- | --- |
| [Replace All Text](actions/replace-all-text.md) | GET | Replaces all matching text with Power Assist. |

### Slugified String

| Action | Method | Description |
| --- | --- | --- |
| [Slugify String](actions/slugify-string.md) | GET | Converts a string into a slug with Power Assist. |

### Sorted Array

| Action | Method | Description |
| --- | --- | --- |
| [Sort Array](actions/sort-array.md) | GET | Sorts an array with Power Assist. |

### Sorted Objects

| Action | Method | Description |
| --- | --- | --- |
| [Sort Array By Property](actions/sort-array-by-property.md) | GET | Sorts an array by property with Power Assist. |

### String Chunks

| Action | Method | Description |
| --- | --- | --- |
| [Chop String](actions/chop-string.md) | GET | Chops a string into chunks with Power Assist. |

### String Parts

| Action | Method | Description |
| --- | --- | --- |
| [Split String Into Words](actions/split-string-into-words.md) | GET | Splits a string into words with Power Assist. |

### Substring Count

| Action | Method | Description |
| --- | --- | --- |
| [Count Substring Instances](actions/count-substring-instances.md) | GET | Counts substring matches with Power Assist. |

### Trimmed String

| Action | Method | Description |
| --- | --- | --- |
| [Trim String](actions/trim-string.md) | GET | Trims a string with Power Assist. |

### Unescaped Html

| Action | Method | Description |
| --- | --- | --- |
| [Unescape HTML](actions/unescape-html.md) | GET | Unescapes HTML entities with Power Assist. |

### Word Count

| Action | Method | Description |
| --- | --- | --- |
| [Count Words](actions/count-words.md) | GET | Counts words in a string with Power Assist. |

