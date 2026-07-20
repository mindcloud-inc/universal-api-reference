# TouchBasePro: Delete SMS List

Deletes an existing SMS list from TouchBasePro.

```
DELETE https://connect.mindcloud.co/v1/universal/touchBasePro/latest/actions/delete-sms-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TouchBasePro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/touchBasePro/latest/actions/delete-sms-list?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/touchBasePro/latest/actions/delete-sms-list?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native TouchBasePro API returns.

## Native endpoint

Through the native TouchBasePro API, this operation is `DELETE /sms/list/{listId}` (base URL `https://api.touchbasepro.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-sms-list.md) for the provider-specific parameters and requirements.

