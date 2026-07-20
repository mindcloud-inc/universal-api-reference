# Create Resource with Schedule It

Creates a new resource in Schedule It.

## Endpoint

- **Method:** `POST`
- **Path:** `/resources`
- **Base URL:** `https://www.scheduleit.com/api`
- **Official documentation:** [Create Resource](https://www.scheduleit.com/faq/10640/is-there-a-rest-api-or-webhooks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The resource name. |
| `owner` | body | `string` | yes | Comma-separated group IDs for the resource owner groups. |
| `email` | body | `string` | no | The resource email address. |
| `data1` | body | `string` | no | The first resource details field. |
| `skills` | body | `string` | no | Comma-separated skill IDs. |
| `geonav` | body | `string` | no | Geo navigation value. |
