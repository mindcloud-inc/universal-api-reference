# Emelia: Get User Data

Retrieves user account data from Emelia.

```
GET https://connect.mindcloud.co/v1/universal/emelia/latest/actions/get-user-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Emelia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/emelia/latest/actions/get-user-data?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/emelia/latest/actions/get-user-data?${params}`, {
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
        "me": {
          "dueInvoice": {},
          "email": "ava@example.com",
          "joinedDate": "2026-05-07T12:00:00.000Z",
          "name": "Ava Chen",
          "picture": {},
          "showMailbox": {},
          "uid": "string"
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.me.dueInvoice` | object |  |
| `data.me.email` | string |  |
| `data.me.joinedDate` | date |  |
| `data.me.name` | string |  |
| `data.me.picture` | object |  |
| `data.me.showMailbox` | object |  |
| `data.me.uid` | string |  |

## Native endpoint

Through the native Emelia API, this operation is `POST /graphql` (base URL `https://graphql.emelia.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-data.md) for the provider-specific parameters and requirements.

