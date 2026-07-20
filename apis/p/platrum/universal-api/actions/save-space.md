# Platrum: Save space

Creates or updates a knowledge space in Platrum.

```
POST https://connect.mindcloud.co/v1/universal/platrum/latest/actions/save-space
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Platrum `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/platrum/latest/actions/save-space" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/platrum/latest/actions/save-space', {
  method: 'POST',
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
| `access_edit[]` | array<object> | no | Edit access rules. |
| `access_rules[]` | array<object> | no | Permission rules. |
| `access[]` | array<object> | no | View access rules. |
| `description` | string | no | Space description. |
| `id` | number | no | Space ID for updates. |
| `is_archived` | boolean | no | Whether the space is archived. |
| `is_public` | boolean | no | Whether the space is public. |
| `slug` | string | no | Space slug. |
| `title` | string | no | Space title. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `status` | string |  |

## Native endpoint

Through the native Platrum API, this operation is `POST /wiki/api/space/save` (base URL `https://3e8e7be.platrum.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/save-space.md) for the provider-specific parameters and requirements.

