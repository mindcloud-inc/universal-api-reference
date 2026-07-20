# ReleaseNotes: Delete Webhook

Deletes a webhook from ReleaseNotes.

```
DELETE https://connect.mindcloud.co/v1/universal/releaseNotes/latest/actions/delete-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ReleaseNotes `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/releaseNotes/latest/actions/delete-webhook?connectionId=$CONNECTION_ID&projectId=11233&webhookId=12345" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "11233",
  "webhookId": "12345"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/releaseNotes/latest/actions/delete-webhook?${params}`, {
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
| `webhookId` | string | yes | The webhook ID returned by the list or create webhook endpoints. Example: `12345`. |

## Response

```json
{
  "success": true,
  "data": [
    {
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
| `message` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native ReleaseNotes API, this operation is `DELETE /projects/:projectId/webhooks/:webhookId` (base URL `https://api.releasenotes.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-webhook.md) for the provider-specific parameters and requirements.

