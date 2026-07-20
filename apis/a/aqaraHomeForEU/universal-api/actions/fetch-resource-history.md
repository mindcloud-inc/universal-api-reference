# Aqara Home for EU: Get Resource History



```
GET https://connect.mindcloud.co/v1/universal/aqaraHomeForEU/latest/actions/fetch-resource-history
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aqara Home for EU `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aqaraHomeForEU/latest/actions/fetch-resource-history?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aqaraHomeForEU/latest/actions/fetch-resource-history?${params}`, {
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
      "message": "string",
      "requestId": "string",
      "result": {
        "data": [
          {
            "time": "2026-05-07T12:00:00.000Z",
            "value": "string"
          }
        ]
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number |  |
| `message` | string |  |
| `requestId` | string |  |
| `result.data[].time` | date |  |
| `result.data[].value` | string |  |

## Native endpoint

Through the native Aqara Home for EU API, this operation is `POST /v3.0/open/api` (base URL `https://open-ger.aqara.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/fetch-resource-history.md) for the provider-specific parameters and requirements.

