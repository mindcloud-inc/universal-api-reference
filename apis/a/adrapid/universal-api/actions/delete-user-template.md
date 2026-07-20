# Adrapid: Delete User Template

Deletes an existing user template from Adrapid.

```
DELETE https://connect.mindcloud.co/v1/universal/adrapid/latest/actions/delete-user-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Adrapid `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/adrapid/latest/actions/delete-user-template?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/adrapid/latest/actions/delete-user-template?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Adrapid API returns.

## Native endpoint

Through the native Adrapid API, this operation is `DELETE /users/:userId/templates/:id` (base URL `https://api.adrapid.com/v1/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-user-template.md) for the provider-specific parameters and requirements.

