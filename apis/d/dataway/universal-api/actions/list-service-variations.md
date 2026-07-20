# Dataway: List Service Variations

Retrieves service variations from Dataway for a selected service.

```
GET https://connect.mindcloud.co/v1/universal/dataway/latest/actions/list-service-variations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dataway `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dataway/latest/actions/list-service-variations?connectionId=$CONNECTION_ID&service_slug=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "service_slug": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dataway/latest/actions/list-service-variations?${params}`, {
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
| `service_slug` | string | yes | Service slug, for example mtn-data. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "amount": 1,
        "fixedPrice": "string",
        "name": "Ava Chen",
        "newAmount": 1,
        "slug": "string",
        "status": "string"
      },
      "responseCode": "string",
      "responseDescription": "string",
      "responseMessage": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | List of service variations. |
| `data.amount` | number | Variation amount. |
| `data.fixedPrice` | string | Whether the variation amount is fixed. |
| `data.name` | string | Variation display name. |
| `data.newAmount` | number | Current variation amount. |
| `data.slug` | string | Variation slug. |
| `data.status` | string | Variation status. |
| `responseCode` | string | Provider response code. |
| `responseDescription` | string | Provider response description. |
| `responseMessage` | string | Provider response message. |

## Native endpoint

Through the native Dataway API, this operation is `GET /get-service-variations` (base URL `https://datawayapp.com/vendor`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-service-variations.md) for the provider-specific parameters and requirements.

