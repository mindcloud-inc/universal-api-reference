# Billforward: Get Credit Note

Retrieves a credit note from Billforward.

```
GET https://connect.mindcloud.co/v1/universal/billforward/latest/actions/get-credit-note
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Billforward `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/billforward/latest/actions/get-credit-note?connectionId=$CONNECTION_ID&creditNoteId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "creditNoteId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/billforward/latest/actions/get-credit-note?${params}`, {
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
| `creditNoteId` | string | yes | The Billforward credit note ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Billforward API returns.

## Native endpoint

Through the native Billforward API, this operation is `GET /credit-notes/:creditNoteId` (base URL `https://app-sandbox.billforward.net/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-credit-note.md) for the provider-specific parameters and requirements.

