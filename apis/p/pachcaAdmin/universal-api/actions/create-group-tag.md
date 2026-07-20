# Pachca (Admin): Create Group Tag

Creates a new group tag in the Pachca Admin API.

```
POST https://connect.mindcloud.co/v1/universal/pachcaAdmin/latest/actions/create-group-tag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pachca (Admin) `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pachcaAdmin/latest/actions/create-group-tag" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "groupTag.name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pachcaAdmin/latest/actions/create-group-tag', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "groupTag.name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `groupTag.name` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "id": 1,
        "name": "Ava Chen",
        "usersCount": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.id` | number |  |
| `data.name` | string |  |
| `data.usersCount` | number |  |

## Native endpoint

Through the native Pachca (Admin) API, this operation is `POST /group_tags` (base URL `https://api.pachca.com/api/shared/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-group-tag.md) for the provider-specific parameters and requirements.

