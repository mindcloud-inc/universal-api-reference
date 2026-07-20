# AnyDB: Get Download URL

Retrieves a download URL for an AnyDB attachment.

```
GET https://connect.mindcloud.co/v1/universal/anyDB/latest/actions/get-download-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AnyDB `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/anyDB/latest/actions/get-download-url?connectionId=$CONNECTION_ID&teamId=string&databaseId=string&recordId=string&cellPosition=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "teamId": "string",
  "databaseId": "string",
  "recordId": "string",
  "cellPosition": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/anyDB/latest/actions/get-download-url?${params}`, {
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
| `teamId` | string | yes | The AnyDB team ID. |
| `databaseId` | string | yes | The AnyDB database ID. |
| `recordId` | string | yes | The AnyDB record ID. |
| `cellPosition` | string | yes | The cell position to download. |
| `redirect` | boolean | no | Whether AnyDB should return an HTTP redirect instead of a JSON payload. |
| `preview` | boolean | no | Whether AnyDB should generate a preview download. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native AnyDB API returns.

## Native endpoint

Through the native AnyDB API, this operation is `GET /api/integrations/ext/download` (base URL `https://app.anydb.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-download-url.md) for the provider-specific parameters and requirements.

