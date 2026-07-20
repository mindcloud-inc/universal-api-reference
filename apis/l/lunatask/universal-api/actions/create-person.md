# Lunatask: Create Person



```
POST https://connect.mindcloud.co/v1/universal/lunatask/latest/actions/create-person
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lunatask `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/lunatask/latest/actions/create-person" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "firstName": "Ava",
  "lastName": "Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lunatask/latest/actions/create-person', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "firstName": "Ava",
    "lastName": "Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `firstName` | string | yes | A person's first name |
| `lastName` | string | yes | A person's last name |
| `relationshipStrength` | string | no | Relationship strength classification for the person |
| `source` | string | no | Identification of the external system where the person is coming from |
| `sourceId` | string | no | The ID of the record in the external system |
| `email` | string | no | The person's email address |
| `birthday` | date | no | The person's birthday |
| `phone` | string | no | The person's phone number |

## Response

```json
{
  "success": true,
  "data": [
    {
      "agreedReconnectOn": "2026-05-07T12:00:00.000Z",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "lastReconnectOn": "2026-05-07T12:00:00.000Z",
      "nextReconnectOn": "2026-05-07T12:00:00.000Z",
      "relationshipDirection": "string",
      "relationshipStrength": "string",
      "sources": [
        "string"
      ],
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agreedReconnectOn` | date |  |
| `createdAt` | date |  |
| `id` | string |  |
| `lastReconnectOn` | date |  |
| `nextReconnectOn` | date |  |
| `relationshipDirection` | string |  |
| `relationshipStrength` | string |  |
| `sources` | array |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Lunatask API, this operation is `POST /people` (base URL `https://api.lunatask.app/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-person.md) for the provider-specific parameters and requirements.

