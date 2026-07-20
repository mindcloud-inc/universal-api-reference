# CheckFlow: Share Checklist



```
PUT https://connect.mindcloud.co/v1/universal/checkFlow/latest/actions/share-checklist
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CheckFlow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/checkFlow/latest/actions/share-checklist" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "checklistId": "1234",
  "isShared": "true"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/checkFlow/latest/actions/share-checklist', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "checklistId": "1234",
    "isShared": "true"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `checklistId` | number | yes | The ID of the checklist. Example: `1234`. |
| `isShared` | boolean | yes | Use true to create a share URL and false to remove it. Example: `true`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "isShared": true,
      "key": "string",
      "name": "Ava Chen",
      "sharedKey": "string",
      "sharedUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `isShared` | boolean |  |
| `key` | string |  |
| `name` | string |  |
| `sharedKey` | string |  |
| `sharedUrl` | string |  |

## Native endpoint

Through the native CheckFlow API, this operation is `POST /api/checklist/share` (base URL `https://app.checkflow.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/share-checklist.md) for the provider-specific parameters and requirements.

