# Asana: Create a status update

Creates a status update in Asana.

```
POST https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/create-a-status-update
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Asana `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/create-a-status-update" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "data": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/create-a-status-update', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "data": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `optFields[]` | array<string> | no |  |
| `data` | object | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdBy": {
        "gid": "string",
        "name": "Ava Chen",
        "resourceType": "string"
      },
      "gid": "string",
      "hearted": true,
      "htmlText": "string",
      "liked": true,
      "modifiedAt": "2026-05-07T12:00:00.000Z",
      "numHearts": 1,
      "numLikes": 1,
      "parent": {
        "gid": "string",
        "name": "Ava Chen",
        "resourceType": "string"
      },
      "resourceSubtype": "string",
      "resourceType": "string",
      "statusType": "string",
      "text": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `createdBy.gid` | string |  |
| `createdBy.name` | string |  |
| `createdBy.resourceType` | string |  |
| `gid` | string |  |
| `hearted` | boolean |  |
| `htmlText` | string |  |
| `liked` | boolean |  |
| `modifiedAt` | date |  |
| `numHearts` | number |  |
| `numLikes` | number |  |
| `parent.gid` | string |  |
| `parent.name` | string |  |
| `parent.resourceType` | string |  |
| `resourceSubtype` | string |  |
| `resourceType` | string |  |
| `statusType` | string |  |
| `text` | string |  |
| `title` | string |  |

## Native endpoint

Through the native Asana API, this operation is `POST status_updates` (base URL `https://app.asana.com/api/1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-a-status-update.md) for the provider-specific parameters and requirements.

