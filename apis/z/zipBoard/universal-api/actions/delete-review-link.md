# zipBoard: Delete Review Link

Deletes an existing review link from zipBoard.

```
DELETE https://connect.mindcloud.co/v1/universal/zipBoard/latest/actions/delete-review-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a zipBoard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/zipBoard/latest/actions/delete-review-link?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zipBoard/latest/actions/delete-review-link?${params}`, {
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
| `id` | string | yes | Review link token ID to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "expireDate": "string",
      "fileid": "string",
      "id": "string",
      "projectid": "string",
      "secure": true,
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `expireDate` | string | Review link expiration date. |
| `fileid` | string | File identifier. |
| `id` | string | Review link identifier. |
| `projectid` | string | Project identifier. |
| `secure` | boolean | Whether the link is secure. |
| `type` | string | Review link type. |

## Native endpoint

Through the native zipBoard API, this operation is `DELETE /shareurl/:id` (base URL `https://app.zipboard.co/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-review-link.md) for the provider-specific parameters and requirements.

