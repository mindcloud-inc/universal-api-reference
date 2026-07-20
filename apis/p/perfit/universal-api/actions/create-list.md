# Perfit: Create List



```
POST https://connect.mindcloud.co/v1/universal/perfit/latest/actions/create-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Perfit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/perfit/latest/actions/create-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "account": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/perfit/latest/actions/create-list', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "account": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `account` | string | yes | Perfit account name. |
| `name` | string | yes | Provisional list name field based on the generic REST create contract; confirm against the full reference before production use. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "activeContacts": 1,
      "activeContactsP": 1,
      "created": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": 1,
      "inactiveContacts": 1,
      "inactiveContactsP": 1,
      "lastMailed": "2026-05-07T12:00:00.000Z",
      "liveContacts": 1,
      "liveContactsP": 1,
      "name": "Ava Chen",
      "quality": 1,
      "tags": [
        {}
      ],
      "totalContacts": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activeContacts` | number |  |
| `activeContactsP` | number |  |
| `created` | date |  |
| `description` | string |  |
| `id` | number |  |
| `inactiveContacts` | number |  |
| `inactiveContactsP` | number |  |
| `lastMailed` | date |  |
| `liveContacts` | number |  |
| `liveContactsP` | number |  |
| `name` | string |  |
| `quality` | number |  |
| `tags` | array<object> |  |
| `totalContacts` | number |  |

## Native endpoint

Through the native Perfit API, this operation is `POST /:account/lists` (base URL `https://api.myperfit.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-list.md) for the provider-specific parameters and requirements.

