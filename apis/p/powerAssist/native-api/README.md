# Power Assist: Native API Reference

A consolidated summary of Power Assist's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://learn.microsoft.com/en-us/connectors/powerassist/
- **API base URL:** `https://power-assist.p.rapidapi.com`

## Authentication

### RapidAPI Key

Authenticate with the RapidApi Key from the subscribed Power Assist API on RapidAPI.

### Credentials

- **RapidApi Key:** `apiKey` · required

Send these headers with each API request:

```http
X-RapidAPI-Key: <apiKey>
```

[Official authentication documentation](https://learn.microsoft.com/en-us/connectors/powerassist/)

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
| [Calculate Average](actions/calculate-average.md) | `POST /api/math/average` | [docs](https://rapidapi.com/elevate-digital-elevate-digital-default/api/power-assist) |
| [Calculate Median](actions/calculate-median.md) | `POST /api/math/median` | [docs](https://rapidapi.com/elevate-digital-elevate-digital-default/api/power-assist) |
| [Check Any Array Item](actions/check-any-array-item.md) | `POST /api/array/any` | [docs](https://rapidapi.com/elevate-digital-elevate-digital-default/api/power-assist) |
| [Check Every Array Item](actions/check-every-array-item.md) | `POST /api/array/every` | [docs](https://rapidapi.com/elevate-digital-elevate-digital-default/api/power-assist) |
| [Chop String](actions/chop-string.md) | `POST /api/string/chop` | [docs](https://rapidapi.com/elevate-digital-elevate-digital-default/api/power-assist) |
| [Clean Whitespace](actions/clean-whitespace.md) | `POST /api/string/clean` | [docs](https://rapidapi.com/elevate-digital-elevate-digital-default/api/power-assist) |
| [Count Substring Instances](actions/count-substring-instances.md) | `POST /api/string/countInstances` | [docs](https://rapidapi.com/elevate-digital-elevate-digital-default/api/power-assist) |
| [Count Words](actions/count-words.md) | `POST /api/string/wordCount` | [docs](https://rapidapi.com/elevate-digital-elevate-digital-default/api/power-assist) |
| [Escape HTML](actions/escape-html.md) | `POST /api/string/escapeHtml` | [docs](https://rapidapi.com/elevate-digital-elevate-digital-default/api/power-assist) |
| [Filter Array](actions/filter-array.md) | `POST /api/array/filter` | [docs](https://rapidapi.com/elevate-digital-elevate-digital-default/api/power-assist) |
| [Find First Array Item](actions/find-first-array-item.md) | `POST /api/array/findFirst` | [docs](https://rapidapi.com/elevate-digital-elevate-digital-default/api/power-assist) |
| [Group Array By Property](actions/group-array-by-property.md) | `POST /api/array/groupBy` | [docs](https://rapidapi.com/elevate-digital-elevate-digital-default/api/power-assist) |
| [Prepend To Array](actions/prepend-to-array.md) | `POST /api/array/prepend` | [docs](https://rapidapi.com/elevate-digital-elevate-digital-default/api/power-assist) |
| [Remove First Array Item](actions/remove-first-array-item.md) | `POST /api/array/removeFirst` | [docs](https://rapidapi.com/elevate-digital-elevate-digital-default/api/power-assist) |
| [Replace All Text](actions/replace-all-text.md) | `POST /api/string/replaceAll` | [docs](https://rapidapi.com/elevate-digital-elevate-digital-default/api/power-assist) |
| [Replace Text With Regex](actions/replace-text-with-regex.md) | `POST /api/string/regexReplace` | [docs](https://rapidapi.com/elevate-digital-elevate-digital-default/api/power-assist) |
| [Slugify String](actions/slugify-string.md) | `POST /api/string/slugify` | [docs](https://rapidapi.com/elevate-digital-elevate-digital-default/api/power-assist) |
| [Sort Array](actions/sort-array.md) | `POST /api/array/sort` | [docs](https://rapidapi.com/elevate-digital-elevate-digital-default/api/power-assist) |
| [Sort Array By Property](actions/sort-array-by-property.md) | `POST /api/array/sortByProperty` | [docs](https://rapidapi.com/elevate-digital-elevate-digital-default/api/power-assist) |
| [Split String Into Words](actions/split-string-into-words.md) | `POST /api/string/words` | [docs](https://rapidapi.com/elevate-digital-elevate-digital-default/api/power-assist) |
| [Strip HTML](actions/strip-html.md) | `POST /api/string/stripHtml` | [docs](https://rapidapi.com/elevate-digital-elevate-digital-default/api/power-assist) |
| [Trim String](actions/trim-string.md) | `POST /api/string/trim` | [docs](https://rapidapi.com/elevate-digital-elevate-digital-default/api/power-assist) |
| [Unescape HTML](actions/unescape-html.md) | `POST /api/string/unescapeHtml` | [docs](https://rapidapi.com/elevate-digital-elevate-digital-default/api/power-assist) |
| [Validate Email](actions/validate-email.md) | `POST /api/validate/email` | [docs](https://rapidapi.com/elevate-digital-elevate-digital-default/api/power-assist) |
