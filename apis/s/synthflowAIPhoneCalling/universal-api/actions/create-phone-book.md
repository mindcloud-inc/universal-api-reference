# Synthflow AI Phone Calling: Create Phone Book

Creates a new phone book in Synthflow.

```
POST https://connect.mindcloud.co/v1/universal/synthflowAIPhoneCalling/latest/actions/create-phone-book
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Synthflow AI Phone Calling `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/synthflowAIPhoneCalling/latest/actions/create-phone-book" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/synthflowAIPhoneCalling/latest/actions/create-phone-book', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | The phone book name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "key": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `key` | string |  |

## Native endpoint

Through the native Synthflow AI Phone Calling API, this operation is `POST /phonebooks` (base URL `https://api.synthflow.ai/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-phone-book.md) for the provider-specific parameters and requirements.

