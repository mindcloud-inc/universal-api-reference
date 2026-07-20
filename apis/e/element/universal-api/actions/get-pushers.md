# Element: Get Pushers

Retrieves push notification pushers from Element.

```
GET https://connect.mindcloud.co/v1/universal/element/latest/actions/get-pushers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Element `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/element/latest/actions/get-pushers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/element/latest/actions/get-pushers?${params}`, {
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
      "pushers": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `pushers` | array<object> |  |

## Native endpoint

Through the native Element API, this operation is `GET /_matrix/client/v3/pushers` (base URL `{{credentials.homeserverUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-pushers.md) for the provider-specific parameters and requirements.

