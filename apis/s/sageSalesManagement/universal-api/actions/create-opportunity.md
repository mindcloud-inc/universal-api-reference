# Sage Sales Management: Create Opportunity

Creates an opportunity in Sage Sales Management.

```
POST https://connect.mindcloud.co/v1/universal/sageSalesManagement/latest/actions/create-opportunity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sage Sales Management `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sageSalesManagement/latest/actions/create-opportunity" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "salesRepId": "string",
  "salesProbability": 1,
  "reference": "string",
  "statusId": 1,
  "branchId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sageSalesManagement/latest/actions/create-opportunity', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "salesRepId": "string",
    "salesProbability": 1,
    "reference": "string",
    "statusId": 1,
    "branchId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `salesRepId` | string | yes | Sales representative ID |
| `salesProbability` | number | yes | Opportunity sales probability required by ForceManager when creating an opportunity. |
| `reference` | string | yes | Opportunity reference required by ForceManager when creating an opportunity. |
| `statusId` | number | yes | Opportunity status identifier required by ForceManager when creating an opportunity. |
| `branchId` | number | yes | Branch identifier required by ForceManager when creating an opportunity. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "Message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number | Created entity ID |
| `Message` | string | Mutation result message |

## Native endpoint

Through the native Sage Sales Management API, this operation is `POST /opportunities` (base URL `https://api.forcemanager.com/api/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-opportunity.md) for the provider-specific parameters and requirements.

