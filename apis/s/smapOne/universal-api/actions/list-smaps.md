# smapOne: List smaps

Retrieves smaps from smapOne.

```
GET https://connect.mindcloud.co/v1/universal/smapOne/latest/actions/list-smaps
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a smapOne `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smapOne/latest/actions/list-smaps?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smapOne/latest/actions/list-smaps?${params}`, {
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
      "lastPublishedVersion": {},
      "name": "Ava Chen",
      "smapId": "string",
      "totalDataCount": 1,
      "totalOpenTasksCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `lastPublishedVersion` | object |  |
| `name` | string |  |
| `smapId` | string |  |
| `totalDataCount` | number |  |
| `totalOpenTasksCount` | number |  |

## Native endpoint

Through the native smapOne API, this operation is `GET /v1/Smaps` (base URL `https://platform.smapone.com/Backend`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-smaps.md) for the provider-specific parameters and requirements.

