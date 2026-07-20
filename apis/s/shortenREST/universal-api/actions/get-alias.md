# Shorten.REST: Get Alias

Retrieves alias details from Shorten.REST by alias and domain.

```
GET https://connect.mindcloud.co/v1/universal/shortenREST/latest/actions/get-alias
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shorten.REST `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shortenREST/latest/actions/get-alias?connectionId=$CONNECTION_ID&aliasName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "aliasName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shortenREST/latest/actions/get-alias?${params}`, {
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
| `domainName` | string | no | The domain which the alias belongs to, without http/https or trailing slash. |
| `aliasName` | string | yes | The alias value without a leading slash. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": 1,
      "destinations": [
        {}
      ],
      "domainName": "Ava Chen",
      "metatags": [
        {}
      ],
      "name": "Ava Chen",
      "snippets": [
        {}
      ],
      "updatedAt": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | number | Alias creation timestamp in milliseconds. |
| `destinations` | array<object> | Destination routing rules for the alias. |
| `domainName` | string | Domain that owns the alias. |
| `metatags` | array<object> | Alias-specific metatag entries. |
| `name` | string | Alias name. |
| `snippets` | array<object> | Alias-specific snippet entries. |
| `updatedAt` | number | Alias update timestamp in milliseconds. |

## Native endpoint

Through the native Shorten.REST API, this operation is `GET /aliases` (base URL `https://api.shorten.rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-alias.md) for the provider-specific parameters and requirements.

