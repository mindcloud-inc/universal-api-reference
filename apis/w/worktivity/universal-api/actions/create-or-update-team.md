# Worktivity: Create or Update Team

Creates or updates a team in Worktivity.

```
PUT https://connect.mindcloud.co/v1/universal/worktivity/latest/actions/create-or-update-team
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Worktivity `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/worktivity/latest/actions/create-or-update-team" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/worktivity/latest/actions/create-or-update-team', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "created": true,
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | boolean | Whether Worktivity created a new team. |
| `id` | string | Created or updated team ID. |

## Native endpoint

Through the native Worktivity API, this operation is `POST /Team/AddOrUpdate` (base URL `https://open-api.useworktivity.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-or-update-team.md) for the provider-specific parameters and requirements.

