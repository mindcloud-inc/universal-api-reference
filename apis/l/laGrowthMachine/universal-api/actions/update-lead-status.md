# LaGrowthMachine: Update Lead Status

Updates a lead's status in LaGrowthMachine.

```
PUT https://connect.mindcloud.co/v1/universal/laGrowthMachine/latest/actions/update-lead-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LaGrowthMachine `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/laGrowthMachine/latest/actions/update-lead-status" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "campaign[]": [
    "string"
  ],
  "status": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/laGrowthMachine/latest/actions/update-lead-status', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "campaign[]": ["string"],
    "status": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `campaign[]` | array<string> | yes | Campaign name list to scope the status update to. |
| `from` | string | no | Optional status update source. |
| `memberEmail` | string | no | Optional member email used with the `from` field. |
| `persoEmail` | string | no | Lead personal email used to identify the lead. |
| `proEmail` | string | no | Lead professional email used to identify the lead. |
| `status` | string | yes | New lead status value. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "logs": [
        {
          "campaign": "string",
          "leadStatus": "string",
          "leadUpdated": true,
          "reason": "string"
        }
      ],
      "statusCode": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `logs[].campaign` | string | Campaign name processed by the status update request. |
| `logs[].leadStatus` | string | Final lead status after the update. |
| `logs[].leadUpdated` | boolean | Whether the lead status was changed for that campaign. |
| `logs[].reason` | string | Reason returned when the provider does not change the lead status. |
| `statusCode` | number | Provider status code returned after the lead status update. |

## Native endpoint

Through the native LaGrowthMachine API, this operation is `POST /leads/status` (base URL `https://apiv2.lagrowthmachine.com/flow`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-lead-status.md) for the provider-specific parameters and requirements.

