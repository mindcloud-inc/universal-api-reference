# BASIC: Update project details

Updates existing project details in BASIC.

```
PUT https://connect.mindcloud.co/v1/universal/bASIC/latest/actions/update-project-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BASIC `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/bASIC/latest/actions/update-project-details" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bASIC/latest/actions/update-project-details', {
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
      "data": {
        "id": "string",
        "name": "Ava Chen",
        "profile": {},
        "slug": "string",
        "updated_at": "2026-05-07T12:00:00.000Z",
        "website": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.id` | string |  |
| `data.name` | string |  |
| `data.profile` | object |  |
| `data.slug` | string |  |
| `data.updated_at` | date |  |
| `data.website` | string |  |

## Native endpoint

Through the native BASIC API, this operation is `PATCH /project/{id}` (base URL `https://api.basic.tech`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-project-details.md) for the provider-specific parameters and requirements.

