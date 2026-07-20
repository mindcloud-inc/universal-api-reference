# Go4Clients: Update Group

Updates an existing contact group in Go4Clients.

```
PUT https://connect.mindcloud.co/v1/universal/go4Clients/latest/actions/update-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Go4Clients `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/go4Clients/latest/actions/update-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "_id": "string",
  "groupName": "Ava Chen",
  "filterParameters[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/go4Clients/latest/actions/update-group', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "_id": "string",
    "groupName": "Ava Chen",
    "filterParameters[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `_id` | string | yes | ID of the group to update. |
| `groupName` | string | yes | Updated group name. |
| `filterParameters[]` | array<object> | yes | Group filter definitions. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_id": "string",
      "createdOn": "string",
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
      "lastUpdate": "string",
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
| `createdOn` | string |  |
| `filterParameters[].canonicalFilterClass` | string |  |
| `filterParameters[].filterClass` | string |  |
| `filterParameters[].key` | string |  |
| `filterParameters[].type` | string |  |
| `filterParameters[].value` | string |  |
| `groupName` | string |  |
| `lastUpdate` | string |  |
| `organizationId` | string |  |
| `organizationName` | string |  |
| `source` | string |  |
| `userId` | string |  |
| `userName` | string |  |
| `whitelabelId` | string |  |

## Native endpoint

Through the native Go4Clients API, this operation is `PUT /api/groupscontacts/groups/v1.0/` (base URL `https://cloud.go4clients.com:8580`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-group.md) for the provider-specific parameters and requirements.

