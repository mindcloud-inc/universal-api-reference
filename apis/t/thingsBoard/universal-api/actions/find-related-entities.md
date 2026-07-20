# ThingsBoard: Find Related Entities

Finds entities related to a record in ThingsBoard.

```
GET https://connect.mindcloud.co/v1/universal/thingsBoard/latest/actions/find-related-entities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ThingsBoard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/thingsBoard/latest/actions/find-related-entities?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/thingsBoard/latest/actions/find-related-entities?${params}`, {
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
      "": [
        {
          "from": {
            "entityType": "string",
            "id": "string"
          },
          "to": {
            "entityType": "string",
            "id": "string"
          },
          "type": "string",
          "typeGroup": "string",
          "version": 1
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `[].from.entityType` | string |  |
| `[].from.id` | string |  |
| `[].to.entityType` | string |  |
| `[].to.id` | string |  |
| `[].type` | string |  |
| `[].typeGroup` | string |  |
| `[].version` | number |  |

## Native endpoint

Through the native ThingsBoard API, this operation is `POST /relations` (base URL `{{credentials.baseUrl}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-related-entities.md) for the provider-specific parameters and requirements.

