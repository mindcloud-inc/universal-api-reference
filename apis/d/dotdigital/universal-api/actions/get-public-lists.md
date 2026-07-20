# Dotdigital: Get Public Lists

Retrieves all public lists from Dotdigital.

```
GET https://connect.mindcloud.co/v1/universal/dotdigital/latest/actions/get-public-lists
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dotdigital `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dotdigital/latest/actions/get-public-lists?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dotdigital/latest/actions/get-public-lists?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Dotdigital API returns.

## Native endpoint

Through the native Dotdigital API, this operation is `GET /v2/address-books/public` (base URL `https://r2-api.dotmailer.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-public-lists.md) for the provider-specific parameters and requirements.

