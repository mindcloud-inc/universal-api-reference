# Crexendo: List Domain Addresses

Retrieves addresses for a domain in Crexendo.

```
GET https://connect.mindcloud.co/v1/universal/crexendo/latest/actions/list-domain-addresses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Crexendo `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/crexendo/latest/actions/list-domain-addresses?connectionId=$CONNECTION_ID&limit=25&offset=0&domain=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "domain": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/crexendo/latest/actions/list-domain-addresses?${params}`, {
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

Through the native Crexendo API, this operation is `GET /domains/:domain/addresses` (base URL `https://ns-api.com/ns-api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-domain-addresses.md) for the provider-specific parameters and requirements.

