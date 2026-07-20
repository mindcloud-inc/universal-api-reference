# Pingueen: Get User Info



```
GET https://connect.mindcloud.co/v1/universal/pingueen/latest/actions/get-user-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pingueen `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pingueen/latest/actions/get-user-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pingueen/latest/actions/get-user-info?${params}`, {
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
      "_id": "string",
      "auto_reply": {},
      "business_name": "Ava Chen",
      "conversations": {},
      "email": "ava@example.com",
      "language": "string",
      "meta_info": [
        {}
      ],
      "name": "Ava Chen",
      "opening_hours": [
        {}
      ],
      "out_of_hours": {},
      "phone": "string",
      "subscription": "string",
      "surname": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string |  |
| `auto_reply` | object |  |
| `business_name` | string |  |
| `conversations` | object |  |
| `email` | string |  |
| `language` | string |  |
| `meta_info` | array<object> |  |
| `name` | string |  |
| `opening_hours` | array<object> |  |
| `out_of_hours` | object |  |
| `phone` | string |  |
| `subscription` | string |  |
| `surname` | string |  |

## Native endpoint

Through the native Pingueen API, this operation is `GET /me` (base URL `https://api.pingueen.it/ext/v2/{{credentials.businessname}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-info.md) for the provider-specific parameters and requirements.

