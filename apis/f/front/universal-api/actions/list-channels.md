# Front: List Channels

Retrieves a list of channels from Front.

```
GET https://connect.mindcloud.co/v1/universal/front/latest/actions/list-channels
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Front `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/front/latest/actions/list-channels?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/front/latest/actions/list-channels?${params}`, {
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
      "links": {
        "self": "https://example.com"
      },
      "pagination": {
        "next": {}
      },
      "results": [
        {
          "address": "string",
          "id": "string",
          "isPrivate": true,
          "isValid": true,
          "links": {
            "related": {
              "inbox": "https://example.com",
              "owner": "https://example.com"
            },
            "self": "https://example.com"
          },
          "name": "Ava Chen",
          "sendAs": "string",
          "settings": {
            "allTeammatesCanReply": true,
            "undoSendTime": 1
          },
          "type": "string"
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
| `links.self` | string |  |
| `pagination.next` | object |  |
| `results[].address` | string |  |
| `results[].id` | string |  |
| `results[].isPrivate` | boolean |  |
| `results[].isValid` | boolean |  |
| `results[].links.related.inbox` | string |  |
| `results[].links.related.owner` | string |  |
| `results[].links.self` | string |  |
| `results[].name` | string |  |
| `results[].sendAs` | string |  |
| `results[].settings.allTeammatesCanReply` | boolean |  |
| `results[].settings.undoSendTime` | number |  |
| `results[].type` | string |  |

## Native endpoint

Through the native Front API, this operation is `GET /channels` (base URL `https://api2.frontapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-channels.md) for the provider-specific parameters and requirements.

