# Aspire: Create Opportunity Lost Reason

Creates a new opportunity lost reason in your Aspire account.

```
POST https://connect.mindcloud.co/v1/universal/aspire/latest/actions/create-opportunity-lost-reason
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aspire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/aspire/latest/actions/create-opportunity-lost-reason" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "opportunityLostReasonName": "Ava Chen",
  "active": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/aspire/latest/actions/create-opportunity-lost-reason', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "opportunityLostReasonName": "Ava Chen",
    "active": true
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `opportunityLostReasonName` | string | yes |  |
| `active` | boolean | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Aspire API returns.

## Native endpoint

Through the native Aspire API, this operation is `POST OpportunityLostReasons` (base URL `https://{{credentials.environment}}.youraspire.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-opportunity-lost-reason.md) for the provider-specific parameters and requirements.

