# Mixpanel: Delete Annotation

Deletes an existing annotation from Mixpanel.

```
DELETE https://connect.mindcloud.co/v1/universal/mixpanel/latest/actions/delete-annotation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mixpanel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/mixpanel/latest/actions/delete-annotation?connectionId=$CONNECTION_ID&projectId=12345&annotationId=67890" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "12345",
  "annotationId": "67890"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mixpanel/latest/actions/delete-annotation?${params}`, {
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
| `projectId` | number | yes | Mixpanel project ID. Example: `12345`. |
| `annotationId` | number | yes | Annotation ID returned by Mixpanel. Example: `67890`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "results": {
        "id": 1
      },
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `results.id` | number | Deleted annotation ID. |
| `status` | string | Mixpanel response status. |

## Native endpoint

Through the native Mixpanel API, this operation is `DELETE /app/projects/:projectId/annotations/:annotationId` (base URL `https://mixpanel.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-annotation.md) for the provider-specific parameters and requirements.

