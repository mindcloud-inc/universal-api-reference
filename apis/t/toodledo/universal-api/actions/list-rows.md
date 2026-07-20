# Toodledo: List Rows

Retrieves rows from Toodledo.

```
GET https://connect.mindcloud.co/v1/universal/toodledo/latest/actions/list-rows
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Toodledo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/toodledo/latest/actions/list-rows?connectionId=$CONNECTION_ID&list=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "list": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/toodledo/latest/actions/list-rows?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `list` | string | yes | Hexadecimal list ID whose rows should be fetched. |
| `before` | number | no | Return only rows modified before this GMT Unix timestamp. |
| `after` | number | no | Return only rows modified after this GMT Unix timestamp. |
| `id` | string | no | Fetch a single row by its hexadecimal Toodledo row ID. |
| `start` | number | no | Number of records to skip before returning results. |
| `num` | number | no | Maximum number of rows to return. Toodledo documents a default and max of 1000. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "added": 1,
      "cells": {},
      "id": "string",
      "list": "string",
      "modified": 1,
      "version": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `added` | number | Creation timestamp. |
| `cells` | object | Row cell values keyed by column. |
| `id` | string | Row ID. |
| `list` | string | Parent list ID. |
| `modified` | number | Last modification timestamp. |
| `version` | number | Row version number. |

## Native endpoint

Through the native Toodledo API, this operation is `GET /rows/get.php` (base URL `https://api.toodledo.com/3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-rows.md) for the provider-specific parameters and requirements.

