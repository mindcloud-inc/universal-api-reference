# UserBit: Create Or Update Note

Creates or updates a note in UserBit.

```
PUT https://connect.mindcloud.co/v1/universal/userBit/latest/actions/create-or-update-note
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UserBit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/userBit/latest/actions/create-or-update-note" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/userBit/latest/actions/create-or-update-note', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "htmlContent": "string",
      "id": "string",
      "sourceType": "string",
      "textContent": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `htmlContent` | string | HTML note content. |
| `id` | string | Note identifier. |
| `sourceType` | string | UserBit note source type. |
| `textContent` | string | Plain-text note content. |
| `title` | string | Note title. |

## Native endpoint

Through the native UserBit API, this operation is `POST /v1/notes/create-update` (base URL `https://userbit.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-or-update-note.md) for the provider-specific parameters and requirements.

