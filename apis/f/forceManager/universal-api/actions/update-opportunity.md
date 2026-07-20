# ForceManager: Update Opportunity

Updates an existing opportunity in ForceManager.

```
PUT https://connect.mindcloud.co/v1/universal/forceManager/latest/actions/update-opportunity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ForceManager `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/forceManager/latest/actions/update-opportunity" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/forceManager/latest/actions/update-opportunity', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | Unique identifier for the opportunity. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": "string",
      "amount": 1,
      "closingDateExpected": "2026-05-07T12:00:00.000Z",
      "comments": "string",
      "id": 1,
      "probability": 1,
      "topic": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string | Address line 1 of the opportunity. |
| `amount` | number | Amount of the opportunity. |
| `closingDateExpected` | date | Expected closing date of the opportunity. |
| `comments` | string | Comments for the opportunity. |
| `id` | number | Unique identifier for the opportunity. |
| `probability` | number | Probability of the opportunity. |
| `topic` | string | Topic of the opportunity. |

## Native endpoint

Through the native ForceManager API, this operation is `PUT /opportunities`. The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-opportunity.md) for the provider-specific parameters and requirements.

