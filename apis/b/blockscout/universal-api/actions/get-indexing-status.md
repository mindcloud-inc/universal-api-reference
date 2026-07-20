# Blockscout: Get Indexing Status

Retrieves current indexing status from Blockscout.

```
GET https://connect.mindcloud.co/v1/universal/blockscout/latest/actions/get-indexing-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Blockscout `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/blockscout/latest/actions/get-indexing-status?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/blockscout/latest/actions/get-indexing-status?${params}`, {
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
| `chain_id` | string | no | Default: `10`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "finished_indexing": true,
      "indexed_ratio": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `finished_indexing` | boolean |  |
| `indexed_ratio` | string |  |

## Native endpoint

Through the native Blockscout API, this operation is `GET /:chain_id/api/v2/main-page/indexing-status` (base URL `https://api.blockscout.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-indexing-status.md) for the provider-specific parameters and requirements.

