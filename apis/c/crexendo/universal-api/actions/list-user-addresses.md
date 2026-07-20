# Crexendo: List User Addresses

Retrieves addresses for a user in Crexendo.

```
GET https://connect.mindcloud.co/v1/universal/crexendo/latest/actions/list-user-addresses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Crexendo `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/crexendo/latest/actions/list-user-addresses?connectionId=$CONNECTION_ID&limit=25&offset=0&domain=string&user=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "domain": "string",
  "user": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/crexendo/latest/actions/list-user-addresses?${params}`, {
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
| `domain` | string | yes | Domain identifier, for example apps.mindcloud.co. |
| `user` | string | yes | User extension or identifier, for example 1000. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address-city": "string",
      "address-line-1": "string",
      "address-name": "Ava Chen",
      "address-postal-code": "string",
      "address-state-province-abbreviation": "string",
      "domain": "string",
      "emergency-address-id": "string",
      "user": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address-city` | string |  |
| `address-line-1` | string |  |
| `address-name` | string |  |
| `address-postal-code` | string |  |
| `address-state-province-abbreviation` | string |  |
| `domain` | string |  |
| `emergency-address-id` | string |  |
| `user` | string |  |

## Native endpoint

Through the native Crexendo API, this operation is `GET /domains/:domain/users/:user/addresses` (base URL `https://ns-api.com/ns-api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-user-addresses.md) for the provider-specific parameters and requirements.

