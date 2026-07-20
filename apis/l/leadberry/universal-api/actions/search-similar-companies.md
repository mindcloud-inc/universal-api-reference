# Leadberry: Search Similar Companies



```
GET https://connect.mindcloud.co/v1/universal/leadberry/latest/actions/search-similar-companies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Leadberry `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/leadberry/latest/actions/search-similar-companies?connectionId=$CONNECTION_ID&category=string&country=string&token=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "category": "string",
  "country": "string",
  "token": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/leadberry/latest/actions/search-similar-companies?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `category` | string | yes | Leadberry company category to search similar companies for. |
| `country` | string | yes | Country code or country name for the similar-company search. |
| `token` | string | yes | Leadberry token value read from the app session context. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Leadberry API returns.

## Native endpoint

Through the native Leadberry API, this operation is `POST /data/searchSimilar` (base URL `https://app.leadberry.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-similar-companies.md) for the provider-specific parameters and requirements.

