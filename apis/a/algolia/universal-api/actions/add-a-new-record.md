# Algolia: Add a New Record

Creates a new record in an Algolia index.

```
POST https://connect.mindcloud.co/v1/universal/algolia/latest/actions/add-a-new-record
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Algolia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/algolia/latest/actions/add-a-new-record" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "indexName": "Ava Chen",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/algolia/latest/actions/add-a-new-record', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "indexName": "Ava Chen",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `indexName` | string | yes | The name of the Algolia index. |
| `name` | string | yes | Record name or title. |
| `objectID` | string | no | Unique identifier for the record. Omit it to let Algolia generate one. |
| `category` | string | no | Category value for faceting or filtering. |
| `brand` | string | no | Brand value for the record. |
| `color` | string | no | Color value for the record. |
| `price` | number | no | Numeric price for the record. |
| `isPublished` | boolean | no | Whether the record is published. |
| `tags[]` | array<string> | no | Tag values for the record. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "objectID": "string",
      "taskID": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `objectID` | string |  |
| `taskID` | number |  |

## Native endpoint

Through the native Algolia API, this operation is `POST /1/indexes/:indexName` (base URL `https://{{credentials.applicationId}}.algolia.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-a-new-record.md) for the provider-specific parameters and requirements.

