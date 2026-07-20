# Timeular: Delete Tag

Deletes a tag from your Timeular workspace.

```
DELETE https://connect.mindcloud.co/v1/universal/timeular/latest/actions/delete-tag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timeular `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/timeular/latest/actions/delete-tag?connectionId=$CONNECTION_ID&tagId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "tagId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timeular/latest/actions/delete-tag?${params}`, {
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
| `tagId` | string | yes |  |

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

Through the native Timeular API, this operation is `DELETE /api/v4/tags/:tagId` (base URL `https://api.early.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-tag.md) for the provider-specific parameters and requirements.

