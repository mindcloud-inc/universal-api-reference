# Veryfi: Get devices from blocklist

Retrieves blocked devices from Veryfi.

```
GET https://connect.mindcloud.co/v1/universal/veryfi/latest/actions/get-api-v8-partner-fraud-blocklist
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Veryfi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/veryfi/latest/actions/get-api-v8-partner-fraud-blocklist?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/veryfi/latest/actions/get-api-v8-partner-fraud-blocklist?${params}`, {
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
| `page` | number | no | Default value: 1 The page number. The response is capped to maximum of 50 results per page. |
| `pageSize` | number | no | Default value: 1000 The number of results per page. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "devices": [
        {}
      ],
      "next": "string",
      "previous": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `devices` | array<object> |  |
| `next` | string |  |
| `previous` | string |  |

## Native endpoint

Through the native Veryfi API, this operation is `GET /api/v8/partner/fraud/blocklist` (base URL `https://api.veryfi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-api-v8-partner-fraud-blocklist.md) for the provider-specific parameters and requirements.

