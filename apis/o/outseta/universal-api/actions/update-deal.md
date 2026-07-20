# Outseta: Update Deal

Updates an existing deal in Outseta.

```
PUT https://connect.mindcloud.co/v1/universal/outseta/latest/actions/update-deal
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Outseta `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/outseta/latest/actions/update-deal" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "dealUid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/outseta/latest/actions/update-deal', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "dealUid": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `dealUid` | string | yes |  |
| `name` | string | no |  |
| `dealPipelineStage.uid` | string | no |  |
| `amount` | number | no |  |
| `assignedToPersonClientIdentifier` | string | no |  |
| `account.uid` | string | no |  |
| `dealPeople[].person.uid` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Outseta API returns.

## Native endpoint

Through the native Outseta API, this operation is `PUT /crm/deals/:dealUid` (base URL `https://{{credentials.subdomain}}.outseta.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-deal.md) for the provider-specific parameters and requirements.

