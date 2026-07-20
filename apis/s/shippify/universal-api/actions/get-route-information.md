# Shippify: Get Route Information

Retrieves route details from Shippify by route or delivery ID.

```
GET https://connect.mindcloud.co/v1/universal/shippify/latest/actions/get-route-information
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shippify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shippify/latest/actions/get-route-information?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shippify/latest/actions/get-route-information?${params}`, {
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
| `id` | string | yes | Route identifier to query, or a delivery ID that belongs to the route. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "route": {
        "currencyCode": "string",
        "deliveries": [
          [
            {}
          ]
        ],
        "id": "string",
        "referenceId": "string",
        "status": "string",
        "stepIds": [
          [
            {}
          ]
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
| `route.currencyCode` | string | Route currency code. |
| `route.deliveries[]` | array<object> | Deliveries currently attached to the route. |
| `route.id` | string | Route identifier. |
| `route.referenceId` | string | Route reference identifier. |
| `route.status` | string | Route status. |
| `route.stepIds[]` | array<object> | Route step identifiers. |

## Native endpoint

Through the native Shippify API, this operation is `GET /v1/routes/:id` (base URL `https://api.shippify.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-route-information.md) for the provider-specific parameters and requirements.

