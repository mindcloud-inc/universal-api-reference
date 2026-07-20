# CrowdPower: Add Notes

Updates customer notes in CrowdPower.

```
PUT https://connect.mindcloud.co/v1/universal/crowdPower/latest/actions/add-notes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CrowdPower `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/crowdPower/latest/actions/add-notes" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customerId": "string",
  "notes": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/crowdPower/latest/actions/add-notes', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customerId": "string",
    "notes": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customerId` | string | yes | Customer identifier. |
| `notes` | string | yes | Notes to append to the customer. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "customer_id": "string",
      "notes": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customer_id` | string |  |
| `notes` | string |  |

## Native endpoint

Through the native CrowdPower API, this operation is `PUT customers/:customer_id/notes` (base URL `https://api.crowdpower.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-notes.md) for the provider-specific parameters and requirements.

