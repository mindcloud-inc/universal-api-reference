# Tiledesk: Delete Segment

Deletes a segment from the current Tiledesk project.

```
DELETE https://connect.mindcloud.co/v1/universal/tiledesk/latest/actions/delete-segment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tiledesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/tiledesk/latest/actions/delete-segment?connectionId=$CONNECTION_ID&segmentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "segmentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tiledesk/latest/actions/delete-segment?${params}`, {
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
| `segmentId` | string | yes | The segment identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_id": "string",
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
| `_id` | string |  |
| `message` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Tiledesk API, this operation is `DELETE /{{credentials.projectId}}/segments/:segmentId` (base URL `https://api.tiledesk.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-segment.md) for the provider-specific parameters and requirements.

