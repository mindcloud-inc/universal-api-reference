# Onethread: Mark Notifications Seen



```
GET https://connect.mindcloud.co/v1/universal/onethread/latest/actions/mark-notifications-seen
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Onethread `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/onethread/latest/actions/mark-notifications-seen?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/onethread/latest/actions/mark-notifications-seen?${params}`, {
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
      "$clusterTime": {},
      "electionId": "string",
      "n": 1,
      "nModified": 1,
      "ok": 1,
      "operationTime": "2026-05-07T12:00:00.000Z",
      "opTime": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `$clusterTime` | object |  |
| `electionId` | string |  |
| `n` | number |  |
| `nModified` | number |  |
| `ok` | number |  |
| `operationTime` | date |  |
| `opTime` | object |  |

## Native endpoint

Through the native Onethread API, this operation is `GET /notifications/seen` (base URL `https://api.onethread.app/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/mark-notifications-seen.md) for the provider-specific parameters and requirements.

