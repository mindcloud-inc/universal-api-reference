# Priority Matrix: Update Item Notes

Updates item notes in Priority Matrix.

```
PUT https://connect.mindcloud.co/v1/universal/priorityMatrix/latest/actions/update-item-notes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Priority Matrix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/priorityMatrix/latest/actions/update-item-notes" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "descriptionText": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/priorityMatrix/latest/actions/update-item-notes', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "descriptionText": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | Priority Matrix item ID. |
| `descriptionText` | string | yes | Plain text item notes. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "completionPercentage": 1,
      "creationDate": 1,
      "descriptionText": "string",
      "id": 1,
      "name": "Ava Chen",
      "owner": "string",
      "quadrant": 1,
      "resource_uri": "string",
      "state": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `completionPercentage` | number |  |
| `creationDate` | number |  |
| `descriptionText` | string |  |
| `id` | number |  |
| `name` | string |  |
| `owner` | string |  |
| `quadrant` | number |  |
| `resource_uri` | string |  |
| `state` | number |  |

## Native endpoint

Through the native Priority Matrix API, this operation is `PUT /api/v1/item/:id/` (base URL `https://sync.appfluence.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-item-notes.md) for the provider-specific parameters and requirements.

