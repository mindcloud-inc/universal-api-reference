# Dachser: Get Routing

Retrieves routing details for a destination from Dachser.

```
GET https://connect.mindcloud.co/v1/universal/dachser/latest/actions/get-routing
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dachser `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dachser/latest/actions/get-routing?connectionId=$CONNECTION_ID&branchId=1&countryCode=string&postalCode=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "branchId": "1",
  "countryCode": "string",
  "postalCode": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dachser/latest/actions/get-routing?${params}`, {
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
| `branchId` | number | yes | DACHSER dispatch branch number. |
| `division` | string | no | DACHSER division. Use T for industrial goods or F for food. Default: `T`. |
| `countryCode` | string | yes | Consignee ISO country code. |
| `postalCode` | string | yes | Consignee postal code. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "country": "string",
      "printableRelation": "string",
      "relation": {},
      "relationCode": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `country` | string |  |
| `printableRelation` | string |  |
| `relation` | object |  |
| `relationCode` | string |  |

## Native endpoint

Through the native Dachser API, this operation is `GET /rest/v2/routings` (base URL `https://api-gateway.dachser.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-routing.md) for the provider-specific parameters and requirements.

