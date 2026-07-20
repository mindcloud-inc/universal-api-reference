# Apify: Get Private User Data

Retrieves private user data from Apify.

```
GET https://connect.mindcloud.co/v1/universal/apify/latest/actions/get-private-user-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Apify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/apify/latest/actions/get-private-user-data?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/apify/latest/actions/get-private-user-data?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Apify API returns.

## Native endpoint

Through the native Apify API, this operation is `GET /v2/users/me` (base URL `https://api.apify.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-private-user-data.md) for the provider-specific parameters and requirements.

