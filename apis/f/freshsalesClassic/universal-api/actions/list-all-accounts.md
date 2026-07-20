# Freshsales Classic: List All Accounts

Retrieves accounts from a Freshsales Classic view.

```
GET https://connect.mindcloud.co/v1/universal/freshsalesClassic/latest/actions/list-all-accounts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Freshsales Classic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/freshsalesClassic/latest/actions/list-all-accounts?connectionId=$CONNECTION_ID&viewId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "viewId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/freshsalesClassic/latest/actions/list-all-accounts?${params}`, {
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
| `page` | number | no | Page number to return for the selected account view. |
| `viewId` | number | yes | The account view ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "annualRevenue": 1,
      "city": "string",
      "country": "string",
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
| `annualRevenue` | number |  |
| `city` | string |  |
| `country` | string |  |
| `id` | number |  |
| `name` | string |  |
| `numberOfEmployees` | number |  |
| `openDealsAmount` | string |  |
| `openDealsCount` | number |  |
| `phone` | string |  |
| `state` | string |  |
| `tags` | array<string> |  |
| `website` | string |  |
| `wonDealsAmount` | string |  |
| `wonDealsCount` | number |  |

## Native endpoint

Through the native Freshsales Classic API, this operation is `GET /sales_accounts/view/:viewId` (base URL `https://{{credentials.bundleAlias}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-all-accounts.md) for the provider-specific parameters and requirements.

