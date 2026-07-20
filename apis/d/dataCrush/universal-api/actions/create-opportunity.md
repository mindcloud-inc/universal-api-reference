# DataCrush: Create Opportunity

Creates a new opportunity in DataCrush.

```
POST https://connect.mindcloud.co/v1/universal/dataCrush/latest/actions/create-opportunity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DataCrush `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dataCrush/latest/actions/create-opportunity" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Renewal Opportunity",
  "close_date": "string",
  "amount": 1,
  "account_key": "string",
  "stage": "qualification"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dataCrush/latest/actions/create-opportunity', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Renewal Opportunity",
    "close_date": "string",
    "amount": 1,
    "account_key": "string",
    "stage": "qualification"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Opportunity name. Example: `Renewal Opportunity`. |
| `close_date` | string | yes | Close date in YYYY-MM-DD format. |
| `amount` | number | yes | Opportunity amount. |
| `account_key` | string | yes | Account key linked to the opportunity. |
| `stage` | string | yes | Initial opportunity stage. Example: `qualification`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "opportunity_key": "string",
      "result": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `opportunity_key` | string |  |
| `result` | string |  |

## Native endpoint

Through the native DataCrush API, this operation is `POST /crm/opportunity/insert` (base URL `https://api.datacrush.la`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-opportunity.md) for the provider-specific parameters and requirements.

