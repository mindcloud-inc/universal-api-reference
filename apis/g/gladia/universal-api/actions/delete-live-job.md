# Gladia: Delete Live Job

Deletes a live job from Gladia.

```
DELETE https://connect.mindcloud.co/v1/universal/gladia/latest/actions/delete-live-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gladia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/gladia/latest/actions/delete-live-job?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gladia/latest/actions/delete-live-job?${params}`, {
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
| `id` | string | yes | Gladia live job identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deleted": true,
      "id": "string",
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deleted` | boolean |  |
| `id` | string |  |
| `status` | number |  |

## Native endpoint

Through the native Gladia API, this operation is `DELETE /v2/live/:id` (base URL `https://api.gladia.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-live-job.md) for the provider-specific parameters and requirements.

