# ReleaseNotes: Remove Subscriber

Deletes a subscriber from ReleaseNotes.

```
DELETE https://connect.mindcloud.co/v1/universal/releaseNotes/latest/actions/remove-subscriber
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ReleaseNotes `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/releaseNotes/latest/actions/remove-subscriber?connectionId=$CONNECTION_ID&projectId=11233&value=subscriber.one%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "11233",
  "value": "subscriber.one@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/releaseNotes/latest/actions/remove-subscriber?${params}`, {
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
| `projectId` | string | yes | The numeric Project ID shown in ReleaseNotes URLs like /manage/project/1234/releases/4321. Example: `11233`. |
| `value` | string | yes | The subscriber email address or value to remove. Example: `subscriber.one@example.com`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |

## Native endpoint

Through the native ReleaseNotes API, this operation is `POST /projects/:projectId/subscribers/remove` (base URL `https://api.releasenotes.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-subscriber.md) for the provider-specific parameters and requirements.

