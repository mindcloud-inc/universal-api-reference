# Detrack: List Routes By Date

Retrieves routes from Detrack for a specific date.

```
GET https://connect.mindcloud.co/v1/universal/detrack/latest/actions/list-routes-by-date
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Detrack `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/detrack/latest/actions/list-routes-by-date?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/detrack/latest/actions/list-routes-by-date?${params}`, {
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
| `date` | string | no | Route date in YYYY-MM-DD format. |
| `limit` | string | no | Maximum number of routes to return. |
| `page` | string | no | Page number for paginated route results. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Detrack API returns.

## Native endpoint

Through the native Detrack API, this operation is `GET /dn/routes` (base URL `https://app.detrack.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-routes-by-date.md) for the provider-specific parameters and requirements.

