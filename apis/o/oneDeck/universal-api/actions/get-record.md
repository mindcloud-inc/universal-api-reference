# OneDeck: Get Record

Retrieves a record from a specific OneDeck board.

```
GET https://connect.mindcloud.co/v1/universal/oneDeck/latest/actions/get-record
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OneDeck `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oneDeck/latest/actions/get-record?connectionId=$CONNECTION_ID&boardId=1ff5d564-2ea6-4053-8c20-fac2ef32f059&recordId=1ff5d564-2ea6-4053-8c20-fac2ef32f029" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "boardId": "1ff5d564-2ea6-4053-8c20-fac2ef32f059",
  "recordId": "1ff5d564-2ea6-4053-8c20-fac2ef32f029"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oneDeck/latest/actions/get-record?${params}`, {
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
| `boardId` | string | yes | The OneDeck board ID. Example: `1ff5d564-2ea6-4053-8c20-fac2ef32f059`. |
| `recordId` | string | yes | The OneDeck record ID. Example: `1ff5d564-2ea6-4053-8c20-fac2ef32f029`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native OneDeck API returns.

## Native endpoint

Through the native OneDeck API, this operation is `GET /boards/{{boardId}}/records/{{recordId}}` (base URL `https://{{credentials.accountName}}.onedeck.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-record.md) for the provider-specific parameters and requirements.

