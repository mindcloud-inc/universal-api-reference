# Expensify: Update Report Status

Updates a report status in Expensify.

```
PUT https://connect.mindcloud.co/v1/universal/expensify/latest/actions/update-report-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Expensify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/expensify/latest/actions/update-report-status" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "status": "REIMBURSED",
  "reportIdList": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/expensify/latest/actions/update-report-status', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "status": "REIMBURSED",
    "reportIdList": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `status` | string | yes | The target report status. Expensify currently supports REIMBURSED. Default: `REIMBURSED`. |
| `paymentSource` | string | no | Optional payment source label. |
| `reportIdList` | string | yes | Comma-separated report IDs to update. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "reason": "string",
      "reportID": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `reason` | string |  |
| `reportID` | string |  |

## Native endpoint

Through the native Expensify API, this operation is `POST ExpensifyIntegrations` (base URL `https://integrations.expensify.com/Integration-Server/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-report-status.md) for the provider-specific parameters and requirements.

