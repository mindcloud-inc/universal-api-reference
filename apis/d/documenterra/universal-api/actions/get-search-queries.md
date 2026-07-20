# Documenterra: Get Search Queries

Retrieves search query reports from Documenterra.

```
GET https://connect.mindcloud.co/v1/universal/documenterra/latest/actions/get-search-queries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Documenterra `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/documenterra/latest/actions/get-search-queries?connectionId=$CONNECTION_ID&endDate=2026-05-07T12%3A00%3A00.000Z&prLogin=string&startDate=2026-05-07T12%3A00%3A00.000Z" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "endDate": "2026-05-07T12:00:00.000Z",
  "prLogin": "string",
  "startDate": "2026-05-07T12:00:00.000Z"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/documenterra/latest/actions/get-search-queries?${params}`, {
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
| `endDate` | date | yes | ISO 8601 report end timestamp in GMT. |
| `prLogin` | string | yes | Authorized reader login, or '-' for anonymous users. |
| `projectId` | string | no | Optional project identifier filter. |
| `startDate` | date | yes | ISO 8601 report start timestamp in GMT. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Documenterra API returns.

## Native endpoint

Through the native Documenterra API, this operation is `GET /reports/user-events/:prLogin/search-queries` (base URL `https://mindclouddocumenterra.try.documenterra.net/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-search-queries.md) for the provider-specific parameters and requirements.

