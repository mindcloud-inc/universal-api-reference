# Chargeflow: List Evidence

Retrieves dispute evidence from your Chargeflow account.

```
GET https://connect.mindcloud.co/v1/universal/chargeflow/latest/actions/list-evidence
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chargeflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chargeflow/latest/actions/list-evidence?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chargeflow/latest/actions/list-evidence?${params}`, {
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
      "evidences": [
        {
          "account_id": "string",
          "ext_account_id": "string",
          "id": "string",
          "status": "string"
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
| `evidences` | array<object> |  |
| `evidences[].account_id` | string |  |
| `evidences[].ext_account_id` | string |  |
| `evidences[].id` | string |  |
| `evidences[].status` | string |  |
| `pagination.totalCount` | number |  |

## Native endpoint

Through the native Chargeflow API, this operation is `GET /evidence` (base URL `https://api.chargeflow.io/public/2025-04-01`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-evidence.md) for the provider-specific parameters and requirements.

