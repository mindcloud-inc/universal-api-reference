# Piloterr: Check Domain Malicious



```
GET https://connect.mindcloud.co/v1/universal/piloterr/latest/actions/check-domain-malicious
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Piloterr `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/piloterr/latest/actions/check-domain-malicious?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/piloterr/latest/actions/check-domain-malicious?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `query` | string | yes | Domain or IP address to check for malicious reports. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "detections": [
        "string"
      ],
      "isMalicious": true,
      "query": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `detections` | array<string> |  |
| `isMalicious` | boolean |  |
| `query` | string |  |

## Native endpoint

Through the native Piloterr API, this operation is `GET /domain/malicious` (base URL `https://api.piloterr.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-domain-malicious.md) for the provider-specific parameters and requirements.

