# Go4Clients: Create Group

Creates a new contact group in Go4Clients.

```
POST https://connect.mindcloud.co/v1/universal/go4Clients/latest/actions/create-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Go4Clients `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/go4Clients/latest/actions/create-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "groupName": "Heavy People",
  "filterParameters[]": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/go4Clients/latest/actions/create-group', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "groupName": "Heavy People",
    "filterParameters[]": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `groupName` | string | yes | Name of the group to create. Example: `Heavy People`. |
| `filterParameters[]` | array<object> | yes | Array of filter objects with key, type, and value. Example: `[object Object]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_id": "string",
      "createdOn": "2026-05-07T12:00:00.000Z",
      "filterParameters": [
        {
          "canonicalFilterClass": "string",
          "filterClass": "string",
          "key": "string",
          "type": "string",
          "value": "string"
        }
      ],
      "groupName": "Ava Chen",
      "lastUpdate": "2026-05-07T12:00:00.000Z",
      "organizationId": "string",
      "organizationName": "Ava Chen",
      "source": "string",
      "userId": "string",
      "userName": "Ava Chen",
      "whitelabelId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string |  |
| `createdOn` | date |  |
| `filterParameters[].canonicalFilterClass` | string |  |
| `filterParameters[].filterClass` | string |  |
| `filterParameters[].key` | string |  |
| `filterParameters[].type` | string |  |
| `filterParameters[].value` | string |  |
| `groupName` | string |  |
| `lastUpdate` | date |  |
| `organizationId` | string |  |
| `organizationName` | string |  |
| `source` | string |  |
| `userId` | string |  |
| `userName` | string |  |
| `whitelabelId` | string |  |

## Native endpoint

Through the native Go4Clients API, this operation is `POST /api/groupscontacts/groups/v1.0/` (base URL `https://cloud.go4clients.com:8580`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-group.md) for the provider-specific parameters and requirements.

