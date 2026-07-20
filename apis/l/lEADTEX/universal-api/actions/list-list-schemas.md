# LEADTEX: List List Schemas

Retrieves list schemas from your LEADTEX account.

```
GET https://connect.mindcloud.co/v1/universal/lEADTEX/latest/actions/list-list-schemas
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LEADTEX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lEADTEX/latest/actions/list-list-schemas?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lEADTEX/latest/actions/list-list-schemas?${params}`, {
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
        "created_at": "2026-05-07T12:00:00.000Z",
        "fields": {},
        "id": "string",
        "is_menu": true,
        "name": "Ava Chen",
        "updated_at": "2026-05-07T12:00:00.000Z"
      },
      "links": {},
      "meta": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |
| `data.created_at` | date |  |
| `data.fields` | object |  |
| `data.id` | string |  |
| `data.is_menu` | boolean |  |
| `data.name` | string |  |
| `data.updated_at` | date |  |
| `links` | object |  |
| `meta` | object |  |

## Native endpoint

Through the native LEADTEX API, this operation is `GET /getListSchemas?api_token={{credentials.apiKey}}` (base URL `https://app.leadteh.ru/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-list-schemas.md) for the provider-specific parameters and requirements.

