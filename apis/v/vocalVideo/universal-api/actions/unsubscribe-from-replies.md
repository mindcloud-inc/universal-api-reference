# Vocal Video: Unsubscribe from Replies

Deletes a reply webhook subscription from Vocal Video.

```
DELETE https://connect.mindcloud.co/v1/universal/vocalVideo/latest/actions/unsubscribe-from-replies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vocal Video `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/vocalVideo/latest/actions/unsubscribe-from-replies?connectionId=$CONNECTION_ID&zapId=123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "zapId": "123"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vocalVideo/latest/actions/unsubscribe-from-replies?${params}`, {
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
| `zapId` | number | yes | Callback id returned by the subscribe action. Example: `123`. |

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
| `success` | boolean | Whether the unsubscribe request completed successfully. |

## Native endpoint

Through the native Vocal Video API, this operation is `DELETE /replies/unsubscribe` (base URL `https://vocalvideo.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/unsubscribe-from-replies.md) for the provider-specific parameters and requirements.

