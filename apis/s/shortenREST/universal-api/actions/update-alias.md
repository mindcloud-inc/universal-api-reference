# Shorten.REST: Update Alias

Updates an existing alias in Shorten.REST.

```
PUT https://connect.mindcloud.co/v1/universal/shortenREST/latest/actions/update-alias
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shorten.REST `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/shortenREST/latest/actions/update-alias" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "aliasName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/shortenREST/latest/actions/update-alias', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "aliasName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `domainName` | string | no | The domain which the alias belongs to, without http/https or trailing slash. |
| `aliasName` | string | yes | The alias value without a leading slash. |
| `destinations` | list<object> | no | Optional list of destination objects. When provided, the full destinations block is replaced. |
| `metatags` | list<object> | no | Optional list of meta tag objects with name and content fields. When provided, the full meta tags block is replaced. |
| `snippets` | list<object> | no | Optional list of snippet objects with id and parameters. When provided, the full snippets block is replaced. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Shorten.REST API returns.

## Native endpoint

Through the native Shorten.REST API, this operation is `PUT /aliases` (base URL `https://api.shorten.rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-alias.md) for the provider-specific parameters and requirements.

