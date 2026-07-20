# Filestage: Start a Review

Starts a review in Filestage.

```
POST https://connect.mindcloud.co/v1/universal/filestage/latest/actions/start-a-review
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Filestage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/filestage/latest/actions/start-a-review" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "versionId": "string",
  "stepId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/filestage/latest/actions/start-a-review', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "versionId": "string",
    "stepId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `versionId` | string | yes |  |
| `stepId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": "2026-05-07T12:00:00.000Z",
      "decisions": [
        {}
      ],
      "dueDate": "2026-05-07T12:00:00.000Z",
      "fileId": "string",
      "id": "string",
      "status": {
        "state": "string"
      },
      "stepId": "string",
      "versionId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | date |  |
| `decisions` | array<object> |  |
| `dueDate` | date |  |
| `fileId` | string |  |
| `id` | string |  |
| `status` | object |  |
| `status.state` | string |  |
| `stepId` | string |  |
| `versionId` | string |  |

## Native endpoint

Through the native Filestage API, this operation is `POST /reviews` (base URL `https://api.filestage.io/ext/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/start-a-review.md) for the provider-specific parameters and requirements.

