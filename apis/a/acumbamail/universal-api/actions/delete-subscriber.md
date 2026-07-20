# Acumbamail: Delete Subscriber

Deletes a subscriber from an Acumbamail list.

```
DELETE https://connect.mindcloud.co/v1/universal/acumbamail/latest/actions/delete-subscriber
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Acumbamail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/acumbamail/latest/actions/delete-subscriber?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/acumbamail/latest/actions/delete-subscriber?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Acumbamail API returns.

## Native endpoint

Through the native Acumbamail API, this operation is `POST /deleteSubscriber/` (base URL `https://acumbamail.com/api/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-subscriber.md) for the provider-specific parameters and requirements.

