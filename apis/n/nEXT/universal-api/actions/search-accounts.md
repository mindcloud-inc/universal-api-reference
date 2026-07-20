# NEXT: Search Accounts

Finds accounts in NEXT by search term.

```
GET https://connect.mindcloud.co/v1/universal/nEXT/latest/actions/search-accounts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NEXT `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nEXT/latest/actions/search-accounts?connectionId=$CONNECTION_ID&searchTerm=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "searchTerm": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nEXT/latest/actions/search-accounts?${params}`, {
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
| `searchTerm` | string | yes | Search text for matching accounts. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native NEXT API returns.

## Native endpoint

Through the native NEXT API, this operation is `GET /search-accounts` (base URL `https://rest.eu-west-1.nextapp.co/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-accounts.md) for the provider-specific parameters and requirements.

