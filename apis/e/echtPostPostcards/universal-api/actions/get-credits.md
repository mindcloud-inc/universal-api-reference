# EchtPost Postcards: Get Credits

Retrieves your account balance from EchtPost Postcards.

```
GET https://connect.mindcloud.co/v1/universal/echtPostPostcards/latest/actions/get-credits
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EchtPost Postcards `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/echtPostPostcards/latest/actions/get-credits?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/echtPostPostcards/latest/actions/get-credits?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native EchtPost Postcards API returns.

## Native endpoint

Through the native EchtPost Postcards API, this operation is `GET /credits` (base URL `https://api.echtpost.de/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-credits.md) for the provider-specific parameters and requirements.

