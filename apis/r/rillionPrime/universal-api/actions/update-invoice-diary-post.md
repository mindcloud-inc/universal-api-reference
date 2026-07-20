# Rillion Prime: Update Invoice Diary Post



```
PUT https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/update-invoice-diary-post
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rillion Prime `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/update-invoice-diary-post" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "invoiceId": 1,
  "diaryId": 1,
  "note": "string",
  "attachedFile": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/update-invoice-diary-post', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "invoiceId": 1,
    "diaryId": 1,
    "note": "string",
    "attachedFile": "string",
    "note": "string",
    "attachedFile": "string",
    "note": "string",
    "attachedFile": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `invoiceId` | number | yes | Path value for InvoiceId. |
| `diaryId` | number | yes | Path value for DiaryId. |
| `note` | string | yes | Request body value for Note. |
| `attachedFile` | string | yes | Request body value for AttachedFile. |
| `note` | string | yes | Request body value for Note. |
| `attachedFile` | string | yes | Request body value for AttachedFile. |
| `note` | string | yes | Request body value for Note. |
| `attachedFile` | string | yes | Request body value for AttachedFile. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Rillion Prime API returns.

## Native endpoint

Through the native Rillion Prime API, this operation is `PUT /invoice/:invoiceId/diary/:diaryId` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-invoice-diary-post.md) for the provider-specific parameters and requirements.

