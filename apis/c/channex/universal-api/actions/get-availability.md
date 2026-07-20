# Channex: Get Availability

Retrieves room type availability from Channex.

```
GET https://connect.mindcloud.co/v1/universal/channex/latest/actions/get-availability
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Channex `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/channex/latest/actions/get-availability?connectionId=$CONNECTION_ID&propertyId=string&dateFrom=2026-05-07T12%3A00%3A00.000Z&dateTo=2026-05-07T12%3A00%3A00.000Z" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "propertyId": "string",
  "dateFrom": "2026-05-07T12:00:00.000Z",
  "dateTo": "2026-05-07T12:00:00.000Z"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/channex/latest/actions/get-availability?${params}`, {
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
| `propertyId` | string | yes | Property UUID used to scope the availability query. |
| `dateFrom` | date | yes | Start date in YYYY-MM-DD format. |
| `dateTo` | date | yes | End date in YYYY-MM-DD format. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Channex API returns.

## Native endpoint

Through the native Channex API, this operation is `GET /availability` (base URL `https://staging.channex.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-availability.md) for the provider-specific parameters and requirements.

