# Nightfall.ai: List Violations

Retrieves violations from Nightfall.ai.

```
GET https://connect.mindcloud.co/v1/universal/nightfallai/latest/actions/list-violations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nightfall.ai `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nightfallai/latest/actions/list-violations?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nightfallai/latest/actions/list-violations?${params}`, {
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
| `createdAfter` | number | no | Unix timestamp in seconds; returns violations created on or after this time. |
| `createdBefore` | number | no | Unix timestamp in seconds; returns violations created before this time. |
| `updatedAfter` | number | no | Unix timestamp in seconds; returns violations updated on or after this time. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "violations": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `violations` | array<object> | Violation results returned by Nightfall. |

## Native endpoint

Through the native Nightfall.ai API, this operation is `GET /dlp/v1/violations` (base URL `https://api.nightfall.ai`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-violations.md) for the provider-specific parameters and requirements.

