# TouchBasePro: Delete SMS Subscriber

Deletes an existing SMS subscriber from TouchBasePro.

```
DELETE https://connect.mindcloud.co/v1/universal/touchBasePro/latest/actions/delete-sms-subscriber
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TouchBasePro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/touchBasePro/latest/actions/delete-sms-subscriber?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/touchBasePro/latest/actions/delete-sms-subscriber?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native TouchBasePro API returns.

## Native endpoint

Through the native TouchBasePro API, this operation is `DELETE /sms/lists/{listId}/subscribers/{number}` (base URL `https://api.touchbasepro.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-sms-subscriber.md) for the provider-specific parameters and requirements.

