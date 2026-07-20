# Optimizely: List Subject Access Requests

Retrieves subject access requests from Optimizely.

```
GET https://connect.mindcloud.co/v1/universal/optimizely/latest/actions/list-subject-access-requests
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Optimizely `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/optimizely/latest/actions/list-subject-access-requests?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/optimizely/latest/actions/list-subject-access-requests?${params}`, {
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
      "accountId": 1,
      "completedAtTime": "string",
      "dataType": "string",
      "expiredAtTime": "string",
      "id": 1,
      "identifier": "string",
      "identifierType": "string",
      "requestedAtTime": "string",
      "requestType": "string",
      "slaDeadlineTime": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | number |  |
| `completedAtTime` | string |  |
| `dataType` | string |  |
| `expiredAtTime` | string |  |
| `id` | number |  |
| `identifier` | string |  |
| `identifierType` | string |  |
| `requestedAtTime` | string |  |
| `requestType` | string |  |
| `slaDeadlineTime` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Optimizely API, this operation is `GET /subject-access-requests` (base URL `https://api.optimizely.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-subject-access-requests.md) for the provider-specific parameters and requirements.

