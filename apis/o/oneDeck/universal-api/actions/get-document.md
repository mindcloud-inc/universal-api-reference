# OneDeck: Get Document

Retrieves a document from OneDeck.

```
GET https://connect.mindcloud.co/v1/universal/oneDeck/latest/actions/get-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OneDeck `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oneDeck/latest/actions/get-document?connectionId=$CONNECTION_ID&documentId=f7bcf3b6-d8a7-4bf9-94d8-2f0d7c5e1234" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "documentId": "f7bcf3b6-d8a7-4bf9-94d8-2f0d7c5e1234"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oneDeck/latest/actions/get-document?${params}`, {
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
| `documentId` | string | yes | Document identifier to retrieve. Example: `f7bcf3b6-d8a7-4bf9-94d8-2f0d7c5e1234`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native OneDeck API returns.

## Native endpoint

Through the native OneDeck API, this operation is `GET /documents/:documentId` (base URL `https://{{credentials.accountName}}.onedeck.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-document.md) for the provider-specific parameters and requirements.

