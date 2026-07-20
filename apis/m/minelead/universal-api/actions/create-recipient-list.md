# Minelead: Create Recipient List

Creates a recipient list in Minelead.

```
POST https://connect.mindcloud.co/v1/universal/minelead/latest/actions/create-recipient-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Minelead `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/minelead/latest/actions/create-recipient-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "listName": "Ava Chen",
  "emails": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/minelead/latest/actions/create-recipient-list', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "listName": "Ava Chen",
    "emails": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `listName` | string | yes | Name of the recipient list to create. |
| `emails` | list<string> | yes | Email addresses to include in the recipient list. Accepts multiple values as an array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "name": "Ava Chen",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `name` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Minelead API, this operation is `POST /campaigns/recipients/` (base URL `https://api.minelead.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-recipient-list.md) for the provider-specific parameters and requirements.

