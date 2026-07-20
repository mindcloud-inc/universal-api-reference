# Late: Preview Queue Slots



```
GET https://connect.mindcloud.co/v1/universal/late/latest/actions/preview-queue-slots
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Late `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/late/latest/actions/preview-queue-slots?connectionId=$CONNECTION_ID&profileId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "profileId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/late/latest/actions/preview-queue-slots?${params}`, {
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
| `profileId` | string | yes |  |
| `queueId` | string | no |  |
| `count` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "profileId": "string",
      "slots": [
        "2026-05-07T12:00:00.000Z"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number | Number of previewed slots. |
| `profileId` | string | Profile identifier. |
| `slots` | array<date> | Upcoming queue slot timestamps. |

## Native endpoint

Through the native Late API, this operation is `GET /queue/preview` (base URL `https://zernio.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/preview-queue-slots.md) for the provider-specific parameters and requirements.

