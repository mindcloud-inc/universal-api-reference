# Samply: Update Project



```
PUT https://connect.mindcloud.co/v1/universal/samply/latest/actions/update-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Samply `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/samply/latest/actions/update-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/samply/latest/actions/update-project', {
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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectid` | string | no | The Samply project id. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "artwork": "string",
      "color": "string",
      "creator": {},
      "id": "string",
      "name": "Ava Chen",
      "object": "string",
      "size": 1,
      "sortBy": {},
      "timeCreated": 1,
      "timeModified": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `artwork` | string |  |
| `color` | string |  |
| `creator` | object |  |
| `id` | string |  |
| `name` | string |  |
| `object` | string |  |
| `size` | number |  |
| `sortBy` | object |  |
| `timeCreated` | number |  |
| `timeModified` | number |  |

## Native endpoint

Through the native Samply API, this operation is `POST /projects/:projectid` (base URL `https://samply.app/api/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-project.md) for the provider-specific parameters and requirements.

