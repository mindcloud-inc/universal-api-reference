# Pinata: Remove File From Group

Deletes a file from a Pinata group.

```
DELETE https://connect.mindcloud.co/v1/universal/pinata/latest/actions/remove-file-from-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pinata `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/pinata/latest/actions/remove-file-from-group?connectionId=$CONNECTION_ID&fileId=string&id=string&network=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fileId": "string",
  "id": "string",
  "network": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pinata/latest/actions/remove-file-from-group?${params}`, {
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
| `fileId` | string | yes | ID of the file to remove from the group. |
| `id` | string | yes | ID of the target group. |
| `network` | string | yes | Target network (`public` or `private`). |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Provider returned null data for the saved successful delete run. |

## Native endpoint

Through the native Pinata API, this operation is `DELETE /v3/groups/:network/:id/ids/:fileId` (base URL `https://api.pinata.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-file-from-group.md) for the provider-specific parameters and requirements.

