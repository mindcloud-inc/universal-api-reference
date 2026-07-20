# SeaTable: Get View

Retrieves a view from a SeaTable base.

```
GET https://connect.mindcloud.co/v1/universal/seaTable/latest/actions/get-view
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SeaTable `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seaTable/latest/actions/get-view?connectionId=$CONNECTION_ID&viewName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "viewName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seaTable/latest/actions/get-view?${params}`, {
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
| `viewName` | string | yes | The SeaTable view name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "colors": {},
      "columnColors": {},
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
| `colors` | object |  |
| `columnColors` | object |  |
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

Through the native SeaTable API, this operation is `GET /api-gateway/api/v2/dtables/:base_uuid/views/:view_name/` (base URL `https://cloud.seatable.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-view.md) for the provider-specific parameters and requirements.

