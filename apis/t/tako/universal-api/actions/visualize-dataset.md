# Tako: Visualize Dataset

Creates a knowledge card from your dataset in Tako.

```
POST https://connect.mindcloud.co/v1/universal/tako/latest/actions/visualize-dataset
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tako `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/tako/latest/actions/visualize-dataset" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tako/latest/actions/visualize-dataset', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fileIds[]` | array<string> | no | One or more connected Tako file IDs to visualize. |
| `query` | string | no | Optional instructions describing the visualization you want Tako to create. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "outputs": {},
      "request_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `outputs` | object | Visualization outputs containing generated knowledge cards and answer text |
| `request_id` | string | Request identifier |

## Native endpoint

Through the native Tako API, this operation is `POST /v1/beta/visualize` (base URL `https://tako.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/visualize-dataset.md) for the provider-specific parameters and requirements.

