# Gridly: List Records

Finds records in a specific Gridly view.

```
GET https://connect.mindcloud.co/v1/universal/gridly/latest/actions/list-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gridly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gridly/latest/actions/list-records?connectionId=$CONNECTION_ID&viewId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "viewId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gridly/latest/actions/list-records?${params}`, {
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
| `viewId` | string | yes | The unique identifier of the view whose records you want to list. |
| `columnIds` | string | no | A comma-separated list of column IDs to include in the response. |
| `fetchFileOption` | string | no | How file cells should be represented. Supported values include `id`, `name`, and `all`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `page` | object | no | Gridly paging object with `offset` and `limit`. |
| `query` | object | no | Gridly filter object keyed by column ID and operator. |
| `sort` | object | no | Gridly sort object keyed by column ID and direction. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cells": [
        {}
      ],
      "id": "string",
      "path": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cells` | array<object> | Cells contained in the record. |
| `id` | string | Record ID. |
| `path` | string | Folder path for the record. |

## Native endpoint

Through the native Gridly API, this operation is `GET /views/:viewId/records` (base URL `https://api.gridly.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-records.md) for the provider-specific parameters and requirements.

