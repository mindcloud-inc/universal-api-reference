# Pushover: Rename Group



```
PUT https://connect.mindcloud.co/v1/universal/pushover/latest/actions/rename-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pushover `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/pushover/latest/actions/rename-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "group": "Pushover group key",
  "name": "On-call Team West"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pushover/latest/actions/rename-group', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "group": "Pushover group key",
    "name": "On-call Team West"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `group` | string | yes | Key of the group to rename. Example: `Pushover group key`. |
| `name` | string | yes | New name for the group. Example: `On-call Team West`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "request": "string",
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `request` | string | Pushover request identifier. |
| `status` | number | API status. Returns 1 when the rename-group request succeeds. |

## Native endpoint

Through the native Pushover API, this operation is `POST /groups/:group/rename.json` (base URL `https://api.pushover.net/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/rename-group.md) for the provider-specific parameters and requirements.

