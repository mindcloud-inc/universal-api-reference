# Adrapid: Update Whitelabel

Updates existing whitelabel settings in Adrapid.

```
PUT https://connect.mindcloud.co/v1/universal/adrapid/latest/actions/update-whitelabel
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Adrapid `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/adrapid/latest/actions/update-whitelabel" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/adrapid/latest/actions/update-whitelabel', {
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

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Adrapid API returns.

## Native endpoint

Through the native Adrapid API, this operation is `PUT /whitelabel/:id` (base URL `https://api.adrapid.com/v1/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-whitelabel.md) for the provider-specific parameters and requirements.

