# Linguin AI: List Supported Languages



```
GET https://connect.mindcloud.co/v1/universal/linguinAI/latest/actions/list-supported-languages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Linguin AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/linguinAI/latest/actions/list-supported-languages?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/linguinAI/latest/actions/list-supported-languages?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Linguin AI API returns.

## Native endpoint

Through the native Linguin AI API, this operation is `GET /v2/languages` (base URL `https://api.linguin.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-supported-languages.md) for the provider-specific parameters and requirements.

