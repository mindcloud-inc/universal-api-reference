# Absinthe: Get User Redemptions

Retrieves a user's redemption history from Absinthe.

```
GET https://connect.mindcloud.co/v1/universal/absinthe/latest/actions/get-user-redemptions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Absinthe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/absinthe/latest/actions/get-user-redemptions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/absinthe/latest/actions/get-user-redemptions?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Absinthe API returns.

## Native endpoint

Through the native Absinthe API, this operation is `GET /redemptions/users/{user_id}/redemptions` (base URL `https://api.absinthe.network`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-redemptions.md) for the provider-specific parameters and requirements.

