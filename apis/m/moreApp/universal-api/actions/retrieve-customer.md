# MoreApp: Retrieve Customer

Retrieves a customer from MoreApp.

```
GET https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/retrieve-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MoreApp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/retrieve-customer?connectionId=$CONNECTION_ID&customerId=209321" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customerId": "209321"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/retrieve-customer?${params}`, {
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
| `customerId` | number | yes | MoreApp customer identifier. Default: `209321`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "customerId": 1,
      "id": "string",
      "logoAssetId": "string",
      "meta": {},
      "name": "Ava Chen",
      "partnerId": "string",
      "plugins": {},
      "regionId": "string",
      "settings": {},
      "unlockedFeatures": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customerId` | number |  |
| `id` | string |  |
| `logoAssetId` | string |  |
| `meta` | object |  |
| `name` | string |  |
| `partnerId` | string |  |
| `plugins` | object |  |
| `regionId` | string |  |
| `settings` | object |  |
| `unlockedFeatures` | array<string> |  |

## Native endpoint

Through the native MoreApp API, this operation is `GET /api/v1.0/customers/{{customerId}}` (base URL `https://api.moreapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-customer.md) for the provider-specific parameters and requirements.

