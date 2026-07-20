# Extracta.ai: Update Classification

Updates an existing classification in Extracta.ai.

```
PUT https://connect.mindcloud.co/v1/universal/extractaai/latest/actions/update-classification
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Extracta.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/extractaai/latest/actions/update-classification" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "classificationId": "string",
  "classificationDetails": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/extractaai/latest/actions/update-classification', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "classificationId": "string",
    "classificationDetails": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `classificationId` | string | yes | Unique identifier for the classification. |
| `classificationDetails` | object | yes | Object containing the classification fields to update. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "classificationId": "string",
      "status": "string",
      "updatedAt": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `classificationId` | string |  |
| `status` | string |  |
| `updatedAt` | number |  |

## Native endpoint

Through the native Extracta.ai API, this operation is `PATCH /documentClassification/updateClassification` (base URL `https://api.extracta.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-classification.md) for the provider-specific parameters and requirements.

