# Microsoft Dynamics 365 Sales: Create Opportunity



```
POST https://connect.mindcloud.co/v1/universal/microsoftDynamics365Sales/latest/actions/create-opportunity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Dynamics 365 Sales `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/microsoftDynamics365Sales/latest/actions/create-opportunity" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "aspireOpportunityId": 1,
  "fields": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/microsoftDynamics365Sales/latest/actions/create-opportunity', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "aspireOpportunityId": 1,
    "fields": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `aspireOpportunityId` | number | yes | Required positive int32 Aspire OpportunityID. Sent as Dynamics opportunity.grny_aspireid in the POST body; duplicate values are rejected by active alternate key grny_uniqueaspireid. |
| `fields` | object | yes | Required Opportunity JSON object using writable Dataverse logical column names. Include name (max 300). Use verified @odata.bind navigation properties for relationships. Omit grny_aspireid because it is in the URL; exclude statecode/statuscode and other unsupported fields. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "opportunityid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `opportunityid` | string | GUID of the newly created Dynamics Opportunity returned by Prefer: return=representation with $select=opportunityid. |

## Native endpoint

Through the native Microsoft Dynamics 365 Sales API, this operation is `POST /opportunities` (base URL `{{credentials.environmentUrl}}/api/data/v9.2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-opportunity.md) for the provider-specific parameters and requirements.

