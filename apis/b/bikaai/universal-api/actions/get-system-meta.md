# Bika.ai: Get System Meta

Retrieves system metadata from Bika.ai.

```
GET https://connect.mindcloud.co/v1/universal/bikaai/latest/actions/get-system-meta
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bika.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bikaai/latest/actions/get-system-meta?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bikaai/latest/actions/get-system-meta?${params}`, {
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
      "code": 1,
      "data": {
        "appEnv": "string",
        "buildNumber": "string",
        "buildSha": "string",
        "buildTime": "2026-05-07T12:00:00.000Z",
        "headers": {},
        "hostname": "https://example.com",
        "version": "string"
      },
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number |  |
| `data.appEnv` | string |  |
| `data.buildNumber` | string |  |
| `data.buildSha` | string |  |
| `data.buildTime` | date |  |
| `data.headers` | object |  |
| `data.hostname` | string |  |
| `data.version` | string |  |
| `message` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Bika.ai API, this operation is `GET /system/meta` (base URL `https://bika.ai/api/openapi/bika/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-system-meta.md) for the provider-specific parameters and requirements.

