# CrowdPower: Get Customer Pages

Retrieves pages for a customer in CrowdPower.

```
GET https://connect.mindcloud.co/v1/universal/crowdPower/latest/actions/get-customer-pages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CrowdPower `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/crowdPower/latest/actions/get-customer-pages?connectionId=$CONNECTION_ID&customerId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customerId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/crowdPower/latest/actions/get-customer-pages?${params}`, {
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
| `customerId` | string | yes | Customer identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "created_at": 1,
      "first_visited_at": 1,
      "id": "string",
      "last_visited_at": 1,
      "title": "string",
      "updated_at": 1,
      "url": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `created_at` | number |  |
| `first_visited_at` | number |  |
| `id` | string |  |
| `last_visited_at` | number |  |
| `title` | string |  |
| `updated_at` | number |  |
| `url` | object |  |

## Native endpoint

Through the native CrowdPower API, this operation is `GET customers/:customer_id/pages` (base URL `https://api.crowdpower.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-customer-pages.md) for the provider-specific parameters and requirements.

