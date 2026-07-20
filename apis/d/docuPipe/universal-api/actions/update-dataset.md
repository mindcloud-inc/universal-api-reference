# DocuPipe: Update Dataset

Updates a dataset for DocuPipe documents.

```
PUT https://connect.mindcloud.co/v1/universal/docuPipe/latest/actions/update-dataset
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocuPipe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/docuPipe/latest/actions/update-dataset" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "documentIds[]": [
    "string"
  ],
  "dataset": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/docuPipe/latest/actions/update-dataset', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "documentIds[]": ["string"],
    "dataset": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `documentIds[]` | array<string> | yes | List of document IDs to update. |
| `dataset` | string | yes | Name of the dataset to which you want to assign these documents. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean | Whether the dataset update was successful. |

## Native endpoint

Through the native DocuPipe API, this operation is `POST /documents/update-dataset` (base URL `https://app.docupipe.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-dataset.md) for the provider-specific parameters and requirements.

