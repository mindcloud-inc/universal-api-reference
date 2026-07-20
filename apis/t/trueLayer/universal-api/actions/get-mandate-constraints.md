# TrueLayer: Get Mandate Constraints

Retrieves mandate constraints from TrueLayer.

```
GET https://connect.mindcloud.co/v1/universal/trueLayer/latest/actions/get-mandate-constraints
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TrueLayer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/trueLayer/latest/actions/get-mandate-constraints?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/trueLayer/latest/actions/get-mandate-constraints?${params}`, {
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
| `id` | string | yes | TrueLayer mandate ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "expires_at": "string",
      "id": "string",
      "maximum_individual_amount": {},
      "periodic_limits": [
        {}
      ],
      "valid_from": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `expires_at` | string |  |
| `id` | string |  |
| `maximum_individual_amount` | object |  |
| `periodic_limits` | array<object> |  |
| `valid_from` | string |  |

## Native endpoint

Through the native TrueLayer API, this operation is `GET /v3/mandates/:id/constraints` (base URL `https://api.truelayer-sandbox.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-mandate-constraints.md) for the provider-specific parameters and requirements.

