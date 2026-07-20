# List Articles with Reamaze

## Endpoint

- **Method:** `GET`
- **Path:** `/articles`
- **Base URL:** `https://{brand}.reamaze.io/api/v1`
- **Official documentation:** [List Articles](https://www.reamaze.com/api/get_articles)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `status` | query | `string` | no | `status` with `published`, `draft`, or `internal` will show only Published, Draft, or Internal articles respectively. |
| `published` | query | `string` | no | `status` with `published`, `draft`, or `internal` will show only Published, Draft, or Internal articles respectively. |
| `draft` | query | `string` | no | `status` with `published`, `draft`, or `internal` will show only Published, Draft, or Internal articles respectively. |
| `internal` | query | `string` | no | `status` with `published`, `draft`, or `internal` will show only Published, Draft, or Internal articles respectively. |
| `q` | query | `string` | no | `q` with any string will search over articles by keywords. |
