# urlscan.io: Get Incident States

Retrieves states for an incident in urlscan.io.

```
GET https://connect.mindcloud.co/v1/universal/urlscanio/latest/actions/get-incident-states
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a urlscan.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/urlscanio/latest/actions/get-incident-states?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/urlscanio/latest/actions/get-incident-states?${params}`, {
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
      "incidentStates": [
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
| `incidentStates` | array<object> |  |

## Native endpoint

Through the native urlscan.io API, this operation is `GET /api/v1/user/incidentstates/{incidentId}/` (base URL `https://urlscan.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-incident-states.md) for the provider-specific parameters and requirements.

