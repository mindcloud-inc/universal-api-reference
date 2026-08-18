# Centerpoint Universal API Arguments

Arguments are the inputs a Centerpoint action needs. Each [action page](README.md#actions-24) lists its exact keys, types, and required fields. Keys are case-sensitive, and requests with missing or invalid required arguments fail instead of guessing.

## Request format

Pass action arguments as flat fields beside the Universal API controls:

| Piece | Where it goes |
| --- | --- |
| Action fields | `GET` and `DELETE`: query parameters. `POST`, `PUT`, and `PATCH`: JSON body fields. |
| `connectionId` | `GET` and `DELETE`: query string. `POST`, `PUT`, and `PATCH`: JSON body. |
| `limit`, `offset`, `where`, `sort`, `fields` | Query parameters on every HTTP method; never JSON body fields. |

## Data types

| Type | Meaning |
| --- | --- |
| `string` | Text value |
| `number` | Integer or float |
| `boolean` | `true` or `false` |
| `date` | ISO 8601 date-time string |
| `list` | One value from a fixed set (allowed values are listed on the action page) |
| `array` | JSON array; item type noted on the action page |
| `object` | Nested JSON object |
| `file` | File content or reference |

Arguments marked **advanced** are optional tuning knobs; the primary arguments are enough for typical calls. Required arguments are marked on each action page.

## Universal request controls

Beyond each action's own arguments, these parameters work uniformly:

| Parameter | Purpose | Details |
| --- | --- | --- |
| `connectionId` | Which connection to act through | [authentication.md](authentication.md) |
| `limit` / `offset` | Pagination on list actions | [pagination.md](pagination.md) |
| `where` | RSQL filter on list actions | [filtering.md](filtering.md) |
| `sort` | Result ordering on list actions | [sorting.md](sorting.md) |
| `fields` | Response field selection, e.g. `fields=id,name,profile.email` | Works on any read action |

## Field selection

Use the `fields` query parameter to return only the response fields your code reads. Separate fields with commas and use dot notation for nested values:

`fields=id,name,profile.email`

Selection is applied to each row in `data`. The `id` field is retained whenever it exists so rows remain identifiable.

## Responses and errors

Every Centerpoint response uses the same envelope. Single-record actions still return one item inside `data`:

```json
{
  "success": true,
  "data": [
    { "id": "1042", "name": "Ava" }
  ],
  "meta": {}
}
```

Failed requests return `success: false`, a stable `code` your application can branch on, and a human-readable `message`:

```json
{
  "success": false,
  "code": "CONNECTION_APP_MISMATCH",
  "message": "Connection \"conn_123\" is not configured for this app."
}
```

Check the HTTP status first: `400` means the request shape is invalid, `401` or `403` indicates an authentication or authorization problem, and `5xx` means MindCloud could not complete the upstream action.
