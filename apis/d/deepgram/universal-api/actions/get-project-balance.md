# Deepgram: Get Project Balance

Retrieves a project balance from Deepgram.

```
GET https://connect.mindcloud.co/v1/universal/deepgram/latest/actions/get-project-balance
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Deepgram `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deepgram/latest/actions/get-project-balance?connectionId=$CONNECTION_ID&projectId=string&balanceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string",
  "balanceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deepgram/latest/actions/get-project-balance?${params}`, {
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
| `projectId` | string | yes | Deepgram project identifier. |
| `balanceId` | string | yes | Deepgram balance identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "balanceId": "string",
      "purchaseOrderId": "string",
      "units": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number | Outstanding balance amount. |
| `balanceId` | string | Deepgram balance identifier. |
| `purchaseOrderId` | string | Purchase order reference for the balance. |
| `units` | string | Balance units, such as USD. |

## Native endpoint

Through the native Deepgram API, this operation is `GET /v1/projects/:project_id/balances/:balance_id` (base URL `https://api.deepgram.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project-balance.md) for the provider-specific parameters and requirements.

