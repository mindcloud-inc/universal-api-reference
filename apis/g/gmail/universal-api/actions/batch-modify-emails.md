# Google Mail: Batch Modify Emails

Updates labels on multiple Gmail messages.

```
PUT https://connect.mindcloud.co/v1/universal/gmail/latest/actions/batch-modify-emails
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Mail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/gmail/latest/actions/batch-modify-emails" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gmail/latest/actions/batch-modify-emails', {
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
      "addLabelIds": [
        "string"
      ],
      "ids": [
        "string"
      ],
      "removeLabelIds": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addLabelIds` | array<string> |  |
| `ids` | array<string> |  |
| `removeLabelIds` | array<string> |  |

## Native endpoint

Through the native Google Mail API, this operation is `POST /messages/batchModify` (base URL `https://gmail.googleapis.com/gmail/v1/users/:userId`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/batch-modify-emails.md) for the provider-specific parameters and requirements.

