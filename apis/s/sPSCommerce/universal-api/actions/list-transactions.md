# SPS Commerce: List Transactions

Get a list of files in a specified directory.

```
GET https://connect.mindcloud.co/v1/universal/sPSCommerce/latest/actions/list-transactions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SPS Commerce `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sPSCommerce/latest/actions/list-transactions?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sPSCommerce/latest/actions/list-transactions?${params}`, {
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
| `directoryPath` | string | no | Full absolute path to the directory (case sensitive). - Must end with `/` character - Can be empty in case of `root` path |
| `entryNamePrefix` | string | no | Limit the response to entries that begin with the specified prefix (case sensitive) |

## Response

```json
{
  "success": true,
  "data": [
    {
      "path": "string",
      "type": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `path` | string |  |
| `type` | string |  |
| `url` | string |  |

## Native endpoint

Through the native SPS Commerce API, this operation is `GET transactions/v5/data/:directoryPath` (base URL `https://api.spscommerce.com/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-transactions.md) for the provider-specific parameters and requirements.

