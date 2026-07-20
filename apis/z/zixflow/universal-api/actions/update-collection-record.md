# Zixflow: Update Collection Record

Updates an existing collection record in Zixflow.

```
PUT https://connect.mindcloud.co/v1/universal/zixflow/latest/actions/update-collection-record
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zixflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zixflow/latest/actions/update-collection-record" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "collectionId": "string",
  "recordId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zixflow/latest/actions/update-collection-record', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "collectionId": "string",
    "recordId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `collectionId` | string | yes | Collection identifier. |
| `recordId` | string | yes | Record identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "message": "string",
      "status": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Updated collection-record payload returned by Zixflow. |
| `message` | string | Provider success or error message. |
| `status` | boolean | Whether the collection-record update request succeeded. |

## Native endpoint

Through the native Zixflow API, this operation is `PATCH /collection-records/:collectionId/:recordId` (base URL `https://api.zixflow.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-collection-record.md) for the provider-specific parameters and requirements.

