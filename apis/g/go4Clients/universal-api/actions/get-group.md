# Go4Clients: Get Group

Retrieves a contact group from Go4Clients.

```
GET https://connect.mindcloud.co/v1/universal/go4Clients/latest/actions/get-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Go4Clients `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/go4Clients/latest/actions/get-group?connectionId=$CONNECTION_ID&groupId=69dd261660452b001d83ad4b" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "groupId": "69dd261660452b001d83ad4b"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/go4Clients/latest/actions/get-group?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `groupId` | string | yes | Group ID to retrieve. Example: `69dd261660452b001d83ad4b`. |

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
      "showFilterParameters": [
        {
          "canonicalFilterClass": "string",
          "filterClass": "string",
          "key": "string",
          "type": "string",
          "value": "string"
        }
      ],
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
| `showFilterParameters[].canonicalFilterClass` | string |  |
| `showFilterParameters[].filterClass` | string |  |
| `showFilterParameters[].key` | string |  |
| `showFilterParameters[].type` | string |  |
| `showFilterParameters[].value` | string |  |
| `source` | string |  |
| `userId` | string |  |
| `userName` | string |  |
| `whitelabelId` | string |  |

## Native endpoint

Through the native Go4Clients API, this operation is `GET /api/groupscontacts/groups/v1.0/{{groupId}}` (base URL `https://cloud.go4clients.com:8580`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-group.md) for the provider-specific parameters and requirements.

