# Reach360: Get Learning Path

Retrieves a learning path from Reach360 by ID.

```
GET https://connect.mindcloud.co/v1/universal/reach360/latest/actions/get-learning-path
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reach360 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reach360/latest/actions/get-learning-path?connectionId=$CONNECTION_ID&learningPathId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "learningPathId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/reach360/latest/actions/get-learning-path?${params}`, {
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
| `learningPathId` | string | yes | The learning path ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |

## Native endpoint

Through the native Reach360 API, this operation is `GET /learning-paths/:learningPathId` (base URL `https://api.reach360.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-learning-path.md) for the provider-specific parameters and requirements.

