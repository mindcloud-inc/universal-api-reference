# eSign Genie: Update Envelope Recipients

Updates envelope recipients in eSign Genie.

```
PUT https://connect.mindcloud.co/v1/universal/eSignGenie/latest/actions/update-envelope-recipients
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eSign Genie `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/eSignGenie/latest/actions/update-envelope-recipients" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eSignGenie/latest/actions/update-envelope-recipients', {
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

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native eSign Genie API returns.

## Native endpoint

Through the native eSign Genie API, this operation is `POST /folders/updateFolder` (base URL `https://na1.foxitesign.foxit.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-envelope-recipients.md) for the provider-specific parameters and requirements.

