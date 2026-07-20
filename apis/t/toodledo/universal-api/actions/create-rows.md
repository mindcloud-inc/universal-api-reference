# Toodledo: Create Rows

Creates rows in Toodledo.

```
POST https://connect.mindcloud.co/v1/universal/toodledo/latest/actions/create-rows
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Toodledo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/toodledo/latest/actions/create-rows" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "rows": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/toodledo/latest/actions/create-rows', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "rows": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `rows` | string | yes | JSON-encoded array of up to 50 row objects. Each row must include list, cells, and ref. |

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
      "ref": "string",
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
| `ref` | string | Client correlation reference. |
| `version` | number | Row version number. |

## Native endpoint

Through the native Toodledo API, this operation is `POST /rows/add.php` (base URL `https://api.toodledo.com/3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-rows.md) for the provider-specific parameters and requirements.

