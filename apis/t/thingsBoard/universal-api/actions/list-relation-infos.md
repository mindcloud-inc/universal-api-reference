# ThingsBoard: List Relation Infos



```
GET https://connect.mindcloud.co/v1/universal/thingsBoard/latest/actions/list-relation-infos
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ThingsBoard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/thingsBoard/latest/actions/list-relation-infos?connectionId=$CONNECTION_ID&fromId=string&fromType=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fromId": "string",
  "fromType": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/thingsBoard/latest/actions/list-relation-infos?${params}`, {
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
| `fromId` | string | yes | The source entity ID. |
| `fromType` | string | yes | The source entity type, for example DEVICE. |

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
          "fromName": "Ava Chen",
          "to": {
            "entityType": "string",
            "id": "string"
          },
          "toName": "Ava Chen",
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
| `[].fromName` | string |  |
| `[].to.entityType` | string |  |
| `[].to.id` | string |  |
| `[].toName` | string |  |
| `[].type` | string |  |
| `[].typeGroup` | string |  |
| `[].version` | number |  |

## Native endpoint

Through the native ThingsBoard API, this operation is `GET /relations/info` (base URL `{{credentials.baseUrl}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-relation-infos.md) for the provider-specific parameters and requirements.

