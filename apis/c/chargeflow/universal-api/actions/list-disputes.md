# Chargeflow: List Disputes

Retrieves disputes from your Chargeflow account.

```
GET https://connect.mindcloud.co/v1/universal/chargeflow/latest/actions/list-disputes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chargeflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chargeflow/latest/actions/list-disputes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chargeflow/latest/actions/list-disputes?${params}`, {
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
| `limit` | number | no | Maximum number of records to return. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "disputes": [
        {
          "account_id": "string",
          "id": "string",
          "source": "string",
          "source_id": "string"
        }
      ],
      "pagination": {
        "totalCount": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `disputes` | array<object> |  |
| `disputes[].account_id` | string |  |
| `disputes[].id` | string |  |
| `disputes[].source` | string |  |
| `disputes[].source_id` | string |  |
| `pagination.totalCount` | number |  |

## Native endpoint

Through the native Chargeflow API, this operation is `GET /disputes` (base URL `https://api.chargeflow.io/public/2025-04-01`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-disputes.md) for the provider-specific parameters and requirements.

