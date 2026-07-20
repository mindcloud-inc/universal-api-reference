# Search Organizations with ProPublica Nonprofit Explorer

Finds organizations in ProPublica Nonprofit Explorer.

## Endpoint

- **Method:** `GET`
- **Path:** `/search.json`
- **Base URL:** `https://projects.propublica.org/nonprofits/api/v2`
- **Official documentation:** [Search Organizations](https://projects.propublica.org/nonprofits/api/)

## Capabilities

This operation supports [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | no | Keyword search string. Searches organization name, alternate name, and city. Supports quoted phrases, +required terms, and -excluded terms per the official API docs. |
| `page` | query | `number` | no | Zero-indexed page number. The API defaults to 0 and returns 25 results per page. |
| `state[id]` | query | `string` | no | Two-letter U.S. Postal Service state or territory abbreviation. Use ZZ for entities based outside the United States. |
| `ntee[id]` | query | `number` | no | National Taxonomy of Exempt Entities major group integer from 1 through 10. |
| `c_code[id]` | query | `number` | no | Subsection code under section 501(c), or 92 for 4947(a)(1). For example, 3 means 501(c)(3). |
