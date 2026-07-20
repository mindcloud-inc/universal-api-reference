# 5pm: List Priorities

Retrieves task priorities from 5pm.

```
GET https://connect.mindcloud.co/v1/universal/pm/latest/actions/list-priorities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 5pm `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pm/latest/actions/list-priorities?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pm/latest/actions/list-priorities?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "item": [
          {
            "default": "string",
            "id": "string",
            "name": {
              "_cdata": "Ava Chen"
            }
          }
        ]
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.item[].default` | string | Default-priority marker from saved runtime output. |
| `data.item[].id` | string | Priority identifier from saved runtime output. |
| `data.item[].name._cdata` | string | Priority name from saved runtime output. |

## Native endpoint

Through the native 5pm API, this operation is `GET /service/get/metainfo/getPriorities` (base URL `{{credentials.workspaceUrl}}/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-priorities.md) for the provider-specific parameters and requirements.

