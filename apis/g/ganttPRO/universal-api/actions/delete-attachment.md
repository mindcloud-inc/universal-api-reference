# GanttPRO: Delete Attachment

Deletes an existing attachment from GanttPRO.

```
DELETE https://connect.mindcloud.co/v1/universal/ganttPRO/latest/actions/delete-attachment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GanttPRO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/ganttPRO/latest/actions/delete-attachment?connectionId=$CONNECTION_ID&attachmentId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "attachmentId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ganttPRO/latest/actions/delete-attachment?${params}`, {
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
| `attachmentId` | number | yes | GanttPRO attachment identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | string |  |

## Native endpoint

Through the native GanttPRO API, this operation is `DELETE /attachments/:attachmentId` (base URL `https://api.ganttpro.com/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-attachment.md) for the provider-specific parameters and requirements.

