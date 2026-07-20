# Printify: Get Blueprint Shipping

Retrieves blueprint shipping details from Printify.

```
GET https://connect.mindcloud.co/v1/universal/printify/latest/actions/get-blueprint-shipping
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Printify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/printify/latest/actions/get-blueprint-shipping?connectionId=$CONNECTION_ID&blueprintId=5&printProviderId=42" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "blueprintId": "5",
  "printProviderId": "42"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/printify/latest/actions/get-blueprint-shipping?${params}`, {
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
| `blueprintId` | number | yes | Printify blueprint id. Default: `5`. |
| `printProviderId` | number | yes | Printify print provider id. Default: `42`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "handlingTime": {
        "unit": "string",
        "value": 1
      },
      "profiles": [
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
| `handlingTime` | object |  |
| `handlingTime.unit` | string |  |
| `handlingTime.value` | number |  |
| `profiles` | array<object> |  |

## Native endpoint

Through the native Printify API, this operation is `GET /catalog/blueprints/:blueprint_id/print_providers/:print_provider_id/shipping.json` (base URL `https://api.printify.com/v1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-blueprint-shipping.md) for the provider-specific parameters and requirements.

