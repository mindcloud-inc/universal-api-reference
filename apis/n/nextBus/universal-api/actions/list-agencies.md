# NextBus: List Agencies

Retrieves transit agencies from NextBus.

```
GET https://connect.mindcloud.co/v1/universal/nextBus/latest/actions/list-agencies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NextBus `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nextBus/latest/actions/list-agencies?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nextBus/latest/actions/list-agencies?${params}`, {
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
      "regionTitle": "string",
      "shortTitle": "string",
      "tag": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `regionTitle` | string |  |
| `shortTitle` | string |  |
| `tag` | string |  |
| `title` | string |  |

## Native endpoint

Through the native NextBus API, this operation is `GET /publicXMLFeed` (base URL `https://retro.umoiq.com/service`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-agencies.md) for the provider-specific parameters and requirements.

