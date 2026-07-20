# 5pm: List Statuses

Retrieves project statuses from 5pm.

```
GET https://connect.mindcloud.co/v1/universal/pm/latest/actions/list-statuses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 5pm `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pm/latest/actions/list-statuses?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pm/latest/actions/list-statuses?${params}`, {
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
            "alias": {
              "_cdata": "string"
            },
            "id": "string",
            "is_final": "string",
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
| `data.item[].alias._cdata` | string | Status alias from saved runtime output. |
| `data.item[].id` | string | Status identifier from saved runtime output. |
| `data.item[].is_final` | string | Final-state flag from saved runtime output. |
| `data.item[].name._cdata` | string | Status name from saved runtime output. |

## Native endpoint

Through the native 5pm API, this operation is `GET /service/get/metainfo/getStatuses` (base URL `{{credentials.workspaceUrl}}/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-statuses.md) for the provider-specific parameters and requirements.

