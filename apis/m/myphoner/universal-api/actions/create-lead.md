# Myphoner: Create Lead

Creates a new lead in a Myphoner list.

```
POST https://connect.mindcloud.co/v1/universal/myphoner/latest/actions/create-lead
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Myphoner `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/myphoner/latest/actions/create-lead" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "listId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/myphoner/latest/actions/create-lead', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "listId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `listId` | number | yes | The Myphoner list ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "category": "string",
      "claimedAt": "2026-05-07T12:00:00.000Z",
      "claimedBy": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "detectedDuplicates": [
        1
      ],
      "id": 1,
      "ignoredDuplicates": [
        1
      ],
      "lastUpdated": "2026-05-07T12:00:00.000Z",
      "leadData": {},
      "listLocation": "string",
      "listName": "Ava Chen",
      "location": "string",
      "primaryIdentifier": "string",
      "scheduledFor": "2026-05-07T12:00:00.000Z",
      "secondaryIdentifier": "string",
      "state": "string",
      "tertiaryIdentifier": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `category` | string |  |
| `claimedAt` | date |  |
| `claimedBy` | string |  |
| `createdAt` | date |  |
| `detectedDuplicates` | array<number> |  |
| `id` | number |  |
| `ignoredDuplicates` | array<number> |  |
| `lastUpdated` | date |  |
| `leadData` | object |  |
| `listLocation` | string |  |
| `listName` | string |  |
| `location` | string |  |
| `primaryIdentifier` | string |  |
| `scheduledFor` | date |  |
| `secondaryIdentifier` | string |  |
| `state` | string |  |
| `tertiaryIdentifier` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Myphoner API, this operation is `POST /lists/:listId/leads` (base URL `https://{{credentials.subdomain}}.myphoner.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-lead.md) for the provider-specific parameters and requirements.

