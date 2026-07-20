# Freshsales Classic: View an Account

Retrieves an account from Freshsales Classic.

```
GET https://connect.mindcloud.co/v1/universal/freshsalesClassic/latest/actions/view-an-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Freshsales Classic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/freshsalesClassic/latest/actions/view-an-account?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/freshsalesClassic/latest/actions/view-an-account?${params}`, {
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
| `id` | number | yes | The account ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": "string",
      "annualRevenue": 1,
      "city": "string",
      "country": "string",
      "createdAt": "string",
      "domains": [
        "string"
      ],
      "id": 1,
      "name": "Ava Chen",
      "numberOfEmployees": 1,
      "openDealsAmount": "string",
      "openDealsCount": 1,
      "phone": "string",
      "state": "string",
      "tags": [
        "string"
      ],
      "updatedAt": "string",
      "website": "string",
      "wonDealsAmount": "string",
      "wonDealsCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string |  |
| `annualRevenue` | number |  |
| `city` | string |  |
| `country` | string |  |
| `createdAt` | string |  |
| `domains` | array<string> |  |
| `id` | number |  |
| `name` | string |  |
| `numberOfEmployees` | number |  |
| `openDealsAmount` | string |  |
| `openDealsCount` | number |  |
| `phone` | string |  |
| `state` | string |  |
| `tags` | array<string> |  |
| `updatedAt` | string |  |
| `website` | string |  |
| `wonDealsAmount` | string |  |
| `wonDealsCount` | number |  |

## Native endpoint

Through the native Freshsales Classic API, this operation is `GET /sales_accounts/:id` (base URL `https://{{credentials.bundleAlias}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/view-an-account.md) for the provider-specific parameters and requirements.

