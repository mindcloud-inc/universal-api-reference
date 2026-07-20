# Sharetribe: Query Availability Exceptions

Retrieves availability exceptions from Sharetribe.

```
GET https://connect.mindcloud.co/v1/universal/sharetribe/latest/actions/query-availability-exceptions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sharetribe `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sharetribe/latest/actions/query-availability-exceptions?connectionId=$CONNECTION_ID&limit=25&offset=0&listingId=string&start=2026-05-07T12%3A00%3A00.000Z&end=2026-05-07T12%3A00%3A00.000Z" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "listingId": "string",
  "start": "2026-05-07T12:00:00.000Z",
  "end": "2026-05-07T12:00:00.000Z"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sharetribe/latest/actions/query-availability-exceptions?${params}`, {
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
| `listingId` | string | yes | The ID of the listing whose availability exceptions are queried. |
| `start` | date | yes | Query interval start time in ISO 8601 format. |
| `end` | date | yes | Query interval end time in ISO 8601 format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {},
      "id": "string",
      "relationships": {},
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes` | object | Resource attributes payload. |
| `id` | string | Resource ID. |
| `relationships` | object | Resource relationships payload. |
| `type` | string | Resource type. |

## Native endpoint

Through the native Sharetribe API, this operation is `GET availability_exceptions/query` (base URL `https://flex-integ-api.sharetribe.com/v1/integration_api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/query-availability-exceptions.md) for the provider-specific parameters and requirements.

