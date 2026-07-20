# Rownd Data Privacy: Update Group



```
PUT https://connect.mindcloud.co/v1/universal/rowndDataPrivacy/latest/actions/update-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rownd Data Privacy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/rowndDataPrivacy/latest/actions/update-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "group": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rowndDataPrivacy/latest/actions/update-group', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "group": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `group` | string | yes | Rownd group identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "admission_policy": "string",
      "id": "string",
      "member_count": 1,
      "meta": {},
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `admission_policy` | string | How users may join the group. |
| `id` | string | Rownd group identifier. |
| `member_count` | number | Number of members in the group. |
| `meta` | object | Group metadata. |
| `name` | string | Group name. |

## Native endpoint

Through the native Rownd Data Privacy API, this operation is `PUT /groups/:group` (base URL `https://api.rownd.io/applications/{{credentials.appId}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-group.md) for the provider-specific parameters and requirements.

