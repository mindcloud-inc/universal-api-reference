# Extracta.ai: View Classification

Retrieves a classification from Extracta.ai.

```
GET https://connect.mindcloud.co/v1/universal/extractaai/latest/actions/view-classification
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Extracta.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/extractaai/latest/actions/view-classification?connectionId=$CONNECTION_ID&classificationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "classificationId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/extractaai/latest/actions/view-classification?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `classificationId` | string | yes | Unique identifier for the classification. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "classificationDetails": {},
      "classificationId": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `classificationDetails` | object |  |
| `classificationId` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Extracta.ai API, this operation is `POST /documentClassification/viewClassification` (base URL `https://api.extracta.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/view-classification.md) for the provider-specific parameters and requirements.

