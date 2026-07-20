# Refiner: Remove User from Segment

Removes a user from a manual segment in Refiner.

```
DELETE https://connect.mindcloud.co/v1/universal/refiner/latest/actions/remove-user-from-segment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Refiner `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/refiner/latest/actions/remove-user-from-segment?connectionId=$CONNECTION_ID&segmentUuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "segmentUuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/refiner/latest/actions/remove-user-from-segment?${params}`, {
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
| `id` | string | no | Identify the user by your own user ID. |
| `email` | string | no | Identify the user by email address. |
| `segmentUuid` | string | yes | The manual segment UUID to remove the user from. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contactUuid": "string",
      "message": "string",
      "segmentUid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contactUuid` | string |  |
| `message` | string |  |
| `segmentUid` | string |  |

## Native endpoint

Through the native Refiner API, this operation is `DELETE /sync-segment` (base URL `https://api.refiner.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-user-from-segment.md) for the provider-specific parameters and requirements.

