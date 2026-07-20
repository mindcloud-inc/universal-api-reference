# Mixpanel: Create Annotation

Creates a new annotation in Mixpanel.

```
POST https://connect.mindcloud.co/v1/universal/mixpanel/latest/actions/create-annotation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mixpanel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mixpanel/latest/actions/create-annotation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": "12345",
  "date": "2026-03-12 09:30:00",
  "description": "Homepage redesign launched"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mixpanel/latest/actions/create-annotation', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": "12345",
    "date": "2026-03-12 09:30:00",
    "description": "Homepage redesign launched"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | number | yes | Mixpanel project ID. Example: `12345`. |
| `date` | string | yes | Annotation timestamp in YYYY-MM-DD HH:mm:ss format. Example: `2026-03-12 09:30:00`. |
| `description` | string | yes | Annotation text shown in Mixpanel. Example: `Homepage redesign launched`. |
| `tags` | list<number> | no | Optional list of Mixpanel annotation tag IDs. Example: `12,34`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "results": {
        "date": "string",
        "description": "string",
        "id": 1,
        "projectId": 1,
        "tags": [
          [
            "string"
          ]
        ],
        "user": {
          "firstName": "Ava",
          "id": 1,
          "lastName": "Chen"
        }
      },
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `results` | object |  |
| `results.date` | string |  |
| `results.description` | string |  |
| `results.id` | number |  |
| `results.projectId` | number |  |
| `results.tags[]` | array<string> |  |
| `results.user` | object |  |
| `results.user.firstName` | string |  |
| `results.user.id` | number |  |
| `results.user.lastName` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Mixpanel API, this operation is `POST /app/projects/:projectId/annotations` (base URL `https://mixpanel.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-annotation.md) for the provider-specific parameters and requirements.

