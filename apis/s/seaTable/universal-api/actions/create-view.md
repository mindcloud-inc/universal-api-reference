# SeaTable: Create View

Creates a view in a SeaTable base.

```
POST https://connect.mindcloud.co/v1/universal/seaTable/latest/actions/create-view
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SeaTable `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/seaTable/latest/actions/create-view" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/seaTable/latest/actions/create-view', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "colorbys": {},
      "colors": {},
      "filterConjunction": "string",
      "filters": [
        {}
      ],
      "formulaRows": {},
      "groupbys": [
        {}
      ],
      "groupRows": [
        {}
      ],
      "groups": [
        {}
      ],
      "hiddenColumns": [
        {}
      ],
      "id": "string",
      "isLocked": true,
      "linkRows": {},
      "name": "Ava Chen",
      "rows": [
        {}
      ],
      "sorts": [
        {}
      ],
      "summaries": {},
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `colorbys` | object |  |
| `colors` | object |  |
| `filterConjunction` | string |  |
| `filters` | array<object> |  |
| `formulaRows` | object |  |
| `groupbys` | array<object> |  |
| `groupRows` | array<object> |  |
| `groups` | array<object> |  |
| `hiddenColumns` | array<object> |  |
| `id` | string |  |
| `isLocked` | boolean |  |
| `linkRows` | object |  |
| `name` | string |  |
| `rows` | array<object> |  |
| `sorts` | array<object> |  |
| `summaries` | object |  |
| `type` | string |  |

## Native endpoint

Through the native SeaTable API, this operation is `POST /api-gateway/api/v2/dtables/:base_uuid/views/` (base URL `https://cloud.seatable.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-view.md) for the provider-specific parameters and requirements.

