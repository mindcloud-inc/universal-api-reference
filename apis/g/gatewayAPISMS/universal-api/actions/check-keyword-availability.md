# GatewayAPI SMS: Check Keyword Availability

Checks whether a keyword is available in GatewayAPI SMS.

```
GET https://connect.mindcloud.co/v1/universal/gatewayAPISMS/latest/actions/check-keyword-availability
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GatewayAPI SMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gatewayAPISMS/latest/actions/check-keyword-availability?connectionId=$CONNECTION_ID&shortcode=1&keyword=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "shortcode": "1",
  "keyword": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gatewayAPISMS/latest/actions/check-keyword-availability?${params}`, {
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
| `shortcode` | number | yes | Shortcode to check the keyword against. |
| `keyword` | string | yes | Keyword to search for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "available": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `available` | boolean |  |

## Native endpoint

Through the native GatewayAPI SMS API, this operation is `POST /api/vas/check` (base URL `https://gatewayapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-keyword-availability.md) for the provider-specific parameters and requirements.

