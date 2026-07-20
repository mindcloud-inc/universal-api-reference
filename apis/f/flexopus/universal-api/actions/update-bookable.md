# Flexopus: Update Bookable

Updates an existing bookable in Flexopus.

```
PUT https://connect.mindcloud.co/v1/universal/flexopus/latest/actions/update-bookable
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Flexopus `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/flexopus/latest/actions/update-bookable" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/flexopus/latest/actions/update-bookable', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | ID of the bookable object to update. |
| `name` | string | no | Name of the object. |
| `description` | string | no | Description of the object. Set null to clear it. |
| `status` | list<number> | no | Desired status of the object. One of: `0`, `1`. |
| `tags[]` | array<string> | no | Full list of tags to set on the object. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "id": 1,
        "name": "Ava Chen",
        "status": 1,
        "tags": [
          "string"
        ],
        "type": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `data.id` | number |  |
| `data.name` | string |  |
| `data.status` | number |  |
| `data.tags` | array<string> |  |
| `data.type` | number |  |

## Native endpoint

Through the native Flexopus API, this operation is `PATCH /bookables/:id` (base URL `{{credentials.tenantBaseUrl}}/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-bookable.md) for the provider-specific parameters and requirements.

