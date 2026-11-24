# Microsoft Dynamics 365 Sales: Lose Opportunity



```
PUT https://connect.mindcloud.co/v1/universal/microsoftDynamics365Sales/latest/actions/lose-opportunity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Dynamics 365 Sales `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/microsoftDynamics365Sales/latest/actions/lose-opportunity" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/microsoftDynamics365Sales/latest/actions/lose-opportunity', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `opportunityId` | string | no | Dynamics Opportunity GUID; provide this or Aspire Opportunity ID. |
| `aspireOpportunityId` | number | no | Aspire ID resolved by Dynamics alternate key grny_aspireid; provide this or Opportunity ID. |
| `status` | number | no | Win: 3. Lose: 4 (Canceled) or 5 (Out-Sold). Default: `4`. |
| `subject` | string | no | Opportunity Close activity subject. Default: `Lost`. |
| `actualEnd` | string | no | Calendar date exactly as YYYY-MM-DD; no timezone conversion. |
| `description` | string | no | Optional close description. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "message": "string",
      "opportunityId": "string",
      "state": "string",
      "status": 1,
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string | ALREADY_CLOSED when Dynamics reports the Opportunity is already closed. |
| `message` | string | Provider error message when the action fails. |
| `opportunityId` | string | Dynamics GUID or Aspire ID used to identify the Opportunity. |
| `state` | string | Won or Lost. |
| `status` | number | Dynamics status reason. |
| `success` | boolean | Whether the close action completed. |

## Native endpoint

Through the native Microsoft Dynamics 365 Sales API, this operation is `POST /LoseOpportunity` (base URL `{{credentials.environmentUrl}}/api/data/v9.2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/lose-opportunity.md) for the provider-specific parameters and requirements.

