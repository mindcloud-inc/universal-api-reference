# LaunchNotes: Get Announcement Digest



```
GET https://connect.mindcloud.co/v1/universal/launchNotes/latest/actions/get-announcement-digest
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LaunchNotes `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/launchNotes/latest/actions/get-announcement-digest?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/launchNotes/latest/actions/get-announcement-digest?${params}`, {
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
| `id` | string | yes | Announcement digest identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contentType": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "deactivatedAt": "2026-05-07T12:00:00.000Z",
      "emailClickedThroughCount": 1,
      "emailOpenedCount": 1,
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contentType` | string | Digest content type. |
| `createdAt` | date | Digest creation timestamp. |
| `deactivatedAt` | date | Digest deactivation timestamp. |
| `emailClickedThroughCount` | number | Digest email click-through count. |
| `emailOpenedCount` | number | Digest email open count. |
| `id` | string | Announcement digest identifier. |

## Native endpoint

Through the native LaunchNotes API, this operation is `POST /graphql` (base URL `https://app.launchnotes.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-announcement-digest.md) for the provider-specific parameters and requirements.

