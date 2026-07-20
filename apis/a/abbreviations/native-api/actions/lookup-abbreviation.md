# Lookup Abbreviation with Abbreviations

## Endpoint

- **Method:** `GET`
- **Path:** `/abbr.php`
- **Base URL:** `https://www.stands4.com/services/v2`
- **Official documentation:** [Lookup Abbreviation](https://www.abbreviations.com/abbr_api.php)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `term` | query | `string` | yes | The abbreviation or acronym to search for, such as `asap`. |
| `categoryid` | query | `string` | no | Optional STANDS4 category id to search within, such as `MEDICAL`. |
| `sortby` | query | `list` | no | Sort order: popularity, alphabetical, or category. Accepted values: `a`, `c`, `p`. |
