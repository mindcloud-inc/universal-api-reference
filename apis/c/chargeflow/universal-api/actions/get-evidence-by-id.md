# Chargeflow: Get Evidence By ID

Retrieves existing dispute evidence from Chargeflow.

```
GET https://connect.mindcloud.co/v1/universal/chargeflow/latest/actions/get-evidence-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chargeflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chargeflow/latest/actions/get-evidence-by-id?connectionId=$CONNECTION_ID&evidenceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "evidenceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chargeflow/latest/actions/get-evidence-by-id?${params}`, {
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
| `evidenceId` | string | yes | The Chargeflow evidence ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "account_id": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "ext_account_id": "string",
      "file_url": "https://example.com",
      "id": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account_id` | string |  |
| `created_at` | date |  |
| `ext_account_id` | string |  |
| `file_url` | string |  |
| `id` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Chargeflow API, this operation is `GET /evidence/{evidenceId}` (base URL `https://api.chargeflow.io/public/2025-04-01`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-evidence-by-id.md) for the provider-specific parameters and requirements.

