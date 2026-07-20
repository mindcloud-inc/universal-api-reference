# Rossum: Copy Annotation

Copies an annotation to another Rossum queue.

```
PUT https://connect.mindcloud.co/v1/universal/rossum/latest/actions/copy-annotation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rossum `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/rossum/latest/actions/copy-annotation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "annotationID": 1,
  "targetQueue": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rossum/latest/actions/copy-annotation', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "annotationID": 1,
    "targetQueue": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `annotationID` | number | yes |  |
| `targetQueue` | string | yes |  |
| `targetStatus` | string | no |  |
| `reimport` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "annotation": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `annotation` | string | Rossum annotation URL of the copied annotation. |

## Native endpoint

Through the native Rossum API, this operation is `POST /annotations/:annotationID/copy` (base URL `https://mindcloud.rossum.app/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/copy-annotation.md) for the provider-specific parameters and requirements.

