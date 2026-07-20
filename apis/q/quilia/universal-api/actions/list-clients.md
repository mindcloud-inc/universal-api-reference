# Quilia: List Clients



```
GET https://connect.mindcloud.co/v1/universal/quilia/latest/actions/list-clients
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Quilia `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quilia/latest/actions/list-clients?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quilia/latest/actions/list-clients?${params}`, {
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
| `fields` | string | no | Comma-separated list of additional fields to include. Available: address_1, address_2, city, state, postal_code, country, date_of_birth, language, timezone |
| `filter.email` | string | no | Filter by email. See endpoint description for syntax. |
| `filter.name` | string | no | Filter by name. See endpoint description for syntax. |
| `filter.name_first` | string | no | Filter by name_first. See endpoint description for syntax. |
| `filter.name_last` | string | no | Filter by name_last. See endpoint description for syntax. |
| `filter.phone` | string | no | Filter by phone. See endpoint description for syntax. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Quilia API returns.

## Native endpoint

Through the native Quilia API, this operation is `GET clients` (base URL `https://api.quilia.dev/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-clients.md) for the provider-specific parameters and requirements.

