# Evervault: Delete Webhook Endpoint

Deletes an existing webhook endpoint from Evervault.

```
DELETE https://connect.mindcloud.co/v1/universal/evervault/latest/actions/delete-webhook-endpoint
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Evervault `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/evervault/latest/actions/delete-webhook-endpoint?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/evervault/latest/actions/delete-webhook-endpoint?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Evervault API returns.

## Native endpoint

Through the native Evervault API, this operation is `DELETE /webhook-endpoints/{webhook_endpoint_id}` (base URL `https://api.evervault.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-webhook-endpoint.md) for the provider-specific parameters and requirements.

