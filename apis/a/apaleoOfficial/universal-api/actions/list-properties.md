# Apaleo Official: List Properties

Retrieves properties from your Apaleo Official account.

```
GET https://connect.mindcloud.co/v1/universal/apaleoOfficial/latest/actions/list-properties
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Apaleo Official `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/apaleoOfficial/latest/actions/list-properties?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/apaleoOfficial/latest/actions/list-properties?${params}`, {
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
| `status[]` | array<string> | no | Filter properties by lifecycle status. |
| `includeArchived` | boolean | no | Include archived properties in the result set. |
| `countryCode[]` | array<string> | no | Filter properties by ISO country code. |
| `expand[]` | array<string> | no | Expand related nested resources in the response. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Apaleo Official API returns.

## Native endpoint

Through the native Apaleo Official API, this operation is `GET /inventory/v1/properties` (base URL `https://api.apaleo.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-properties.md) for the provider-specific parameters and requirements.

