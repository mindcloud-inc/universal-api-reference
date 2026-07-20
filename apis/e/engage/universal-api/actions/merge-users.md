# Engage: Merge Users

Merges one user into another in Engage.

```
PUT https://connect.mindcloud.co/v1/universal/engage/latest/actions/merge-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Engage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/engage/latest/actions/merge-users" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "source": "string",
  "destination": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/engage/latest/actions/merge-users', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "source": "string",
    "destination": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `source` | string | yes | The user ID to merge from. |
| `destination` | string | yes | The user ID to merge into. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | string | Status returned for the merge request, such as queued. |

## Native endpoint

Through the native Engage API, this operation is `POST /users/merge` (base URL `https://api.engage.so/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/merge-users.md) for the provider-specific parameters and requirements.

