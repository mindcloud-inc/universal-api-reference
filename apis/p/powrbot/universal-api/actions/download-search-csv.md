# Powrbot: Download Search CSV

Retrieves CSV output for a Powrbot bulk search.

```
GET https://connect.mindcloud.co/v1/universal/powrbot/latest/actions/download-search-csv
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Powrbot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/powrbot/latest/actions/download-search-csv?connectionId=$CONNECTION_ID&searchId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "searchId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/powrbot/latest/actions/download-search-csv?${params}`, {
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
| `searchId` | number | yes | Numeric search job identifier. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Powrbot API returns.

## Native endpoint

Through the native Powrbot API, this operation is `GET /search/:searchId/download/` (base URL `https://powrbot.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-search-csv.md) for the provider-specific parameters and requirements.

