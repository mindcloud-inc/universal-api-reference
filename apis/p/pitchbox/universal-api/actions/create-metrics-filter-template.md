# Pitchbox: Create Metrics Filter Template



```
POST https://connect.mindcloud.co/v1/universal/pitchbox/latest/actions/create-metrics-filter-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pitchbox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pitchbox/latest/actions/create-metrics-filter-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pitchbox/latest/actions/create-metrics-filter-template', {
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
| `name` | string | yes | The metrics filter template name. |
| `visibility` | string | no | The metrics filter template visibility. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdBy": {
        "displayName": "Ava Chen",
        "email": "ava@example.com",
        "firstName": "Ava",
        "id": 1,
        "lastName": "Chen"
      },
      "id": 1,
      "name": "Ava Chen",
      "visibility": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `createdBy.displayName` | string |  |
| `createdBy.email` | string |  |
| `createdBy.firstName` | string |  |
| `createdBy.id` | number |  |
| `createdBy.lastName` | string |  |
| `id` | number |  |
| `name` | string |  |
| `visibility` | string |  |

## Native endpoint

Through the native Pitchbox API, this operation is `POST /api/metric_filter_templates` (base URL `https://apiv2.pitchbox.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-metrics-filter-template.md) for the provider-specific parameters and requirements.

