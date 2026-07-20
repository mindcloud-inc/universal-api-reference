# Airlabs: Ping Airlabs

Retrieves API status details from Airlabs.

```
GET https://connect.mindcloud.co/v1/universal/airlabs/latest/actions/ping-airlabs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Airlabs `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/airlabs/latest/actions/ping-airlabs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/airlabs/latest/actions/ping-airlabs?${params}`, {
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
      "request": {},
      "response": "string",
      "terms": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `request` | object | AirLabs request metadata. |
| `response` | string | Ping result returned by AirLabs. |
| `terms` | string | AirLabs terms text returned with the response. |

## Native endpoint

Through the native Airlabs API, this operation is `GET /ping` (base URL `https://airlabs.co/api/v9`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/ping-airlabs.md) for the provider-specific parameters and requirements.

