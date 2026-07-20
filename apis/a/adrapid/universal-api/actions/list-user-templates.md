# Adrapid: List User Templates

Retrieves a user's templates from Adrapid.

```
GET https://connect.mindcloud.co/v1/universal/adrapid/latest/actions/list-user-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Adrapid `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/adrapid/latest/actions/list-user-templates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/adrapid/latest/actions/list-user-templates?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Adrapid API returns.

## Native endpoint

Through the native Adrapid API, this operation is `GET /users/:userId/templates` (base URL `https://api.adrapid.com/v1/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-user-templates.md) for the provider-specific parameters and requirements.

