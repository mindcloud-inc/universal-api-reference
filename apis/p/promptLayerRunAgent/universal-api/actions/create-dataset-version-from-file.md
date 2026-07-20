# PromptLayer Run Agent: Create Dataset Version From File

Creates a dataset version in PromptLayer from a file.

```
POST https://connect.mindcloud.co/v1/universal/promptLayerRunAgent/latest/actions/create-dataset-version-from-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PromptLayer Run Agent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/promptLayerRunAgent/latest/actions/create-dataset-version-from-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "datasetGroupId": "20196",
  "fileName": "dataset.csv",
  "fileContentBase64": "aW5wdXQsZXhwZWN0ZWRfb3V0cHV0CmhlbGxvLHdvcmxkCg=="
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/promptLayerRunAgent/latest/actions/create-dataset-version-from-file', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "datasetGroupId": "20196",
    "fileName": "dataset.csv",
    "fileContentBase64": "aW5wdXQsZXhwZWN0ZWRfb3V0cHV0CmhlbGxvLHdvcmxkCg=="
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `datasetGroupId` | number | yes | ID of the dataset group to add a new dataset version to. Example: `20196`. |
| `fileName` | string | yes | Name of the uploaded file. Example: `dataset.csv`. |
| `fileContentBase64` | string | yes | Base64-encoded file contents for the dataset version. Example: `aW5wdXQsZXhwZWN0ZWRfb3V0cHV0CmhlbGxvLHdvcmxkCg==`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "dataset_id": 1,
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dataset_id` | number |  |
| `message` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native PromptLayer Run Agent API, this operation is `POST /api/public/v2/dataset-versions/from-file` (base URL `https://api.promptlayer.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-dataset-version-from-file.md) for the provider-specific parameters and requirements.

