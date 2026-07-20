# Timeular: Delete Mention

Deletes a mention from your Timeular workspace.

```
DELETE https://connect.mindcloud.co/v1/universal/timeular/latest/actions/delete-mention
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timeular `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/timeular/latest/actions/delete-mention?connectionId=$CONNECTION_ID&mentionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "mentionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timeular/latest/actions/delete-mention?${params}`, {
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
| `mentionId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "timeEntryIds": [
        [
          1
        ]
      ],
      "trackingEdited": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `timeEntryIds[]` | array<number> |  |
| `trackingEdited` | string |  |

## Native endpoint

Through the native Timeular API, this operation is `DELETE /api/v4/mentions/:mentionId` (base URL `https://api.early.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-mention.md) for the provider-specific parameters and requirements.

