# Ortto: Archive Custom Activity



```
DELETE https://connect.mindcloud.co/v1/universal/ortto/latest/actions/archive-custom-activity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ortto `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/ortto/latest/actions/archive-custom-activity?connectionId=$CONNECTION_ID&activityFieldId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "activityFieldId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ortto/latest/actions/archive-custom-activity?${params}`, {
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
| `activityFieldId` | string | yes | Custom activity field ID to archive. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archivedActivity": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archivedActivity` | string |  |

## Native endpoint

Through the native Ortto API, this operation is `DELETE /definitions/activity/delete` (base URL `{{credentials.apiBaseUrl}}/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/archive-custom-activity.md) for the provider-specific parameters and requirements.

