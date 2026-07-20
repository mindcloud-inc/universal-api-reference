# LoginRadius: Create Role

Creates a new role in LoginRadius.

```
POST https://connect.mindcloud.co/v1/universal/loginRadius/latest/actions/create-role
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LoginRadius `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/loginRadius/latest/actions/create-role" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "MindCloudStage3Role"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/loginRadius/latest/actions/create-role', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "MindCloudStage3Role"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Role name to create. Example: `MindCloudStage3Role`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Count": 1,
      "data": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Count` | number | Number of roles returned in the create response. |
| `data` | array<object> | Role records returned by LoginRadius. |

## Native endpoint

Through the native LoginRadius API, this operation is `POST /identity/v2/manage/role` (base URL `https://api.loginradius.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-role.md) for the provider-specific parameters and requirements.

