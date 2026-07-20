# OneSignal: List Segments

Retrieves segments from OneSignal.

```
GET https://connect.mindcloud.co/v1/universal/oneSignal/latest/actions/list-segments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OneSignal `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oneSignal/latest/actions/list-segments?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oneSignal/latest/actions/list-segments?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "appId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "isActive": true,
      "loadingCompletedAt": "2026-05-07T12:00:00.000Z",
      "loadingStartedAt": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "readOnly": true,
      "segmentStatus": "string",
      "source": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `appId` | string | The OneSignal app identifier for the segment. |
| `createdAt` | date | When the segment was created. |
| `id` | string | The segment identifier. |
| `isActive` | boolean | Whether the segment is active. |
| `loadingCompletedAt` | date | When segment loading completed. |
| `loadingStartedAt` | date | When segment loading started. |
| `name` | string | The segment name. |
| `readOnly` | boolean | Whether the segment is read only. |
| `segmentStatus` | string | The current segment status. |
| `source` | string | The segment source. |
| `updatedAt` | date | When the segment was last updated. |

## Native endpoint

Through the native OneSignal API, this operation is `GET /apps/:app_id/segments` (base URL `https://api.onesignal.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-segments.md) for the provider-specific parameters and requirements.

