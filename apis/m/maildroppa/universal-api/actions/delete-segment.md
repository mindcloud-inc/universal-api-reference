# Maildroppa: Delete Segment



```
DELETE https://connect.mindcloud.co/v1/universal/maildroppa/latest/actions/delete-segment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Maildroppa `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/maildroppa/latest/actions/delete-segment?connectionId=$CONNECTION_ID&subscriberSegmentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "subscriberSegmentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/maildroppa/latest/actions/delete-segment?${params}`, {
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
| `subscriberSegmentId` | string | yes | Unique identifier of the segment to remove. |

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
| `success` | boolean | True when delete segment completed. |

## Native endpoint

Through the native Maildroppa API, this operation is `DELETE /subscriber/segment/{subscriberSegmentId}` (base URL `https://api.maildroppa.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-segment.md) for the provider-specific parameters and requirements.

