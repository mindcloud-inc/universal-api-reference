# y.gy: Create Tag

Creates a new tag in y.gy.

```
POST https://connect.mindcloud.co/v1/universal/ygy/latest/actions/create-tag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a y.gy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/ygy/latest/actions/create-tag" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ygy/latest/actions/create-tag', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | The name of the tag to create. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Created At": "string",
      "ID": 1,
      "Name": "Ava Chen",
      "Organization ID": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Created At` | string | When the tag was created. |
| `ID` | number | Unique tag identifier. |
| `Name` | string | Tag name. |
| `Organization ID` | number | Owning organization identifier. |

## Native endpoint

Through the native y.gy API, this operation is `POST /api/v1/tag` (base URL `https://api.y.gy`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-tag.md) for the provider-specific parameters and requirements.

