# Fluents: List Available Numbers

Retrieves available phone numbers from Fluents.

```
GET https://connect.mindcloud.co/v1/universal/fluents/latest/actions/list-available-numbers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fluents `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fluents/latest/actions/list-available-numbers?connectionId=$CONNECTION_ID&limit=1&telephonyProvider=string&telephonyAccountConnection=string&filters=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "limit": "1",
  "telephonyProvider": "string",
  "telephonyAccountConnection": "string",
  "filters": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fluents/latest/actions/list-available-numbers?${params}`, {
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
| `limit` | number | yes | Maximum number of available numbers to return. |
| `telephonyProvider` | string | yes | Telephony provider to search, for example twilio. |
| `telephonyAccountConnection` | string | yes | Fluents telephony account connection ID to source numbers from. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `filters` | string | yes | JSON-encoded Fluents filters string. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "has_more": true,
      "items": [
        {}
      ],
      "page": 1,
      "size": 1,
      "total": 1,
      "total_is_estimated": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `has_more` | boolean |  |
| `items` | array<object> |  |
| `page` | number |  |
| `size` | number |  |
| `total` | number |  |
| `total_is_estimated` | boolean |  |

## Native endpoint

Through the native Fluents API, this operation is `GET /numbers/available` (base URL `https://api.fluents.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-available-numbers.md) for the provider-specific parameters and requirements.

