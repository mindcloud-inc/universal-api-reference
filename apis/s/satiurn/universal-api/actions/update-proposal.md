# Satiurn: Update Proposal

Updates an existing proposal in Satiurn.

```
PUT https://connect.mindcloud.co/v1/universal/satiurn/latest/actions/update-proposal
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Satiurn `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/satiurn/latest/actions/update-proposal" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/satiurn/latest/actions/update-proposal', {
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



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Satiurn API returns.

## Native endpoint

Through the native Satiurn API, this operation is `PUT /proposal/proposal` (base URL `https://publicapi.satiurn.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-proposal.md) for the provider-specific parameters and requirements.

