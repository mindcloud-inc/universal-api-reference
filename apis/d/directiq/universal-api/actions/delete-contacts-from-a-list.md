# DirectIQ: Delete contacts from a list

Deletes contacts from a specific list in DirectIQ.

```
DELETE https://connect.mindcloud.co/v1/universal/directiq/latest/actions/delete-contacts-from-a-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DirectIQ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/directiq/latest/actions/delete-contacts-from-a-list?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/directiq/latest/actions/delete-contacts-from-a-list?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native DirectIQ API returns.

## Native endpoint

Through the native DirectIQ API, this operation is `POST /contacts/lists/deletecontacts/{id}` (base URL `https://rest.directiq.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-contacts-from-a-list.md) for the provider-specific parameters and requirements.

