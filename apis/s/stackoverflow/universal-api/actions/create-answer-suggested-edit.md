# Stackoverflow: Create Answer Suggested Edit

Creates a suggested edit for an answer in Stackoverflow.

```
POST https://connect.mindcloud.co/v1/universal/stackoverflow/latest/actions/create-answer-suggested-edit
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stackoverflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/stackoverflow/latest/actions/create-answer-suggested-edit" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/stackoverflow/latest/actions/create-answer-suggested-edit', {
  method: 'POST',
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
      "comment": "string",
      "creation_date": 1,
      "post_id": 1,
      "suggested_edit_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `comment` | string |  |
| `creation_date` | number |  |
| `post_id` | number |  |
| `suggested_edit_id` | number |  |

## Native endpoint

Through the native Stackoverflow API, this operation is `POST /answers/[:id]/suggested-edit/add` (base URL `https://api.stackexchange.com/2.3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-answer-suggested-edit.md) for the provider-specific parameters and requirements.

