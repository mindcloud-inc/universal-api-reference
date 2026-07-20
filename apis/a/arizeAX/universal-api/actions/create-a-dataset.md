# Arize AX: Create a Dataset

Creates a new dataset in Arize AX.

```
POST https://connect.mindcloud.co/v1/universal/arizeAX/latest/actions/create-a-dataset
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Arize AX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/arizeAX/latest/actions/create-a-dataset" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "examples[]": [
    {}
  ],
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/arizeAX/latest/actions/create-a-dataset', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "examples[]": [{}],
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `examples[]` | array<object> | yes |  |
| `name` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "name": "Ava Chen",
      "space_id": "string",
      "updated_at": "2026-05-07T12:00:00.000Z",
      "versions": [
        {
          "created_at": "2026-05-07T12:00:00.000Z",
          "dataset_id": "string",
          "id": "string",
          "name": "Ava Chen",
          "updated_at": "2026-05-07T12:00:00.000Z"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date |  |
| `id` | string |  |
| `name` | string |  |
| `space_id` | string |  |
| `updated_at` | date |  |
| `versions[].created_at` | date |  |
| `versions[].dataset_id` | string |  |
| `versions[].id` | string |  |
| `versions[].name` | string |  |
| `versions[].updated_at` | date |  |

## Native endpoint

Through the native Arize AX API, this operation is `POST /v2/datasets` (base URL `https://api.arize.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-a-dataset.md) for the provider-specific parameters and requirements.

