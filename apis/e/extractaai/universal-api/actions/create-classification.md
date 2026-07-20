# Extracta.ai: Create Classification

Creates a new classification in Extracta.ai.

```
POST https://connect.mindcloud.co/v1/universal/extractaai/latest/actions/create-classification
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Extracta.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/extractaai/latest/actions/create-classification" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "classificationDetails": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/extractaai/latest/actions/create-classification', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "classificationDetails": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `classificationDetails` | object | yes | Object containing the classification configuration. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "classificationId": "string",
      "createdAt": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `classificationId` | string |  |
| `createdAt` | number |  |
| `status` | string |  |

## Native endpoint

Through the native Extracta.ai API, this operation is `POST /documentClassification/createClassification` (base URL `https://api.extracta.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-classification.md) for the provider-specific parameters and requirements.

