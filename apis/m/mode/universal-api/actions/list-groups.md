# Mode: List Groups

List groups in a Mode workspace.

```
GET https://connect.mindcloud.co/v1/universal/mode/latest/actions/list-groups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mode `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mode/latest/actions/list-groups?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mode/latest/actions/list-groups?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



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
| `memberCount` | number | Number of members in the group. |
| `name` | string | Group name. |
| `spacesCount` | number | Number of collections associated with the group. |
| `state` | string | Group state. |
| `token` | string | Mode group token. |

## Native endpoint

Through the native Mode API, this operation is `GET /groups` (base URL `https://app.mode.com/api/{{credentials.workspace}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-groups.md) for the provider-specific parameters and requirements.

