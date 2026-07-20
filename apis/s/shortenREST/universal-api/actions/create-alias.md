# Shorten.REST: Create Alias

Creates a new alias in Shorten.REST.

```
POST https://connect.mindcloud.co/v1/universal/shortenREST/latest/actions/create-alias
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shorten.REST `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/shortenREST/latest/actions/create-alias" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/shortenREST/latest/actions/create-alias', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `domainName` | string | no | The domain to attach the alias to, without http/https or trailing slash. |
| `aliasName` | string | no | Optional alias value without a leading slash. Leave blank to let Shorten.REST generate one. |
| `destinations` | list<object> | no | List of destination objects. Each object should include at least a url and may also include country or os. |
| `metatags` | list<object> | no | Optional list of meta tag objects with name and content fields. |
| `snippets` | list<object> | no | Optional list of snippet objects with id and parameters. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "aliasName": "Ava Chen",
      "domainName": "Ava Chen",
      "shortUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `aliasName` | string | Created alias name. |
| `domainName` | string | Domain attached to the created alias. |
| `shortUrl` | string | Generated shortened URL. |

## Native endpoint

Through the native Shorten.REST API, this operation is `POST /aliases` (base URL `https://api.shorten.rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-alias.md) for the provider-specific parameters and requirements.

