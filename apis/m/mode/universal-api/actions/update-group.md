# Mode: Update Group

Update a group in a Mode workspace.

```
PUT https://connect.mindcloud.co/v1/universal/mode/latest/actions/update-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mode `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/mode/latest/actions/update-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "groupToken": "string",
  "userGroup": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mode/latest/actions/update-group', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "groupToken": "string",
    "userGroup": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `groupToken` | string | yes | Mode group token. |
| `userGroup` | object | yes | Group fields to update. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "dataSourcesCount": 1,
      "description": "string",
      "groupType": "string",
      "Links": {},
      "managed": true,
      "memberCount": 1,
      "name": "Ava Chen",
      "spacesCount": 1,
      "state": "string",
      "token": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dataSourcesCount` | number | Number of data sources associated with the group. |
| `description` | string | Group description. |
| `groupType` | string | Mode group type. |
| `Links` | object | Mode HAL links. |
| `managed` | boolean | Whether the group is managed. |
| `memberCount` | number | Number of group members. |
| `name` | string | Group name. |
| `spacesCount` | number | Number of collections associated with the group. |
| `state` | string | Group state. |
| `token` | string | Mode group token. |

## Native endpoint

Through the native Mode API, this operation is `PATCH /groups/[:groupToken]` (base URL `https://app.mode.com/api/{{credentials.workspace}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-group.md) for the provider-specific parameters and requirements.

