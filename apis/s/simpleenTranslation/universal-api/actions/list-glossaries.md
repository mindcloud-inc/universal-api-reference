# Simpleen Translation: List Glossaries

Retrieves glossaries from Simpleen Translation.

```
GET https://connect.mindcloud.co/v1/universal/simpleenTranslation/latest/actions/list-glossaries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Simpleen Translation `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/simpleenTranslation/latest/actions/list-glossaries?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/simpleenTranslation/latest/actions/list-glossaries?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Simpleen Translation API returns.

## Native endpoint

Through the native Simpleen Translation API, this operation is `GET /glossaries` (base URL `https://api.simpleen.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-glossaries.md) for the provider-specific parameters and requirements.

