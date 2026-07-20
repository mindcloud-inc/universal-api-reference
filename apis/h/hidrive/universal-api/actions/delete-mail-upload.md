# HiDrive: Delete Mail Upload

Deletes a mail upload from HiDrive.

```
DELETE https://connect.mindcloud.co/v1/universal/hidrive/latest/actions/delete-mail-upload
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HiDrive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/hidrive/latest/actions/delete-mail-upload?connectionId=$CONNECTION_ID&path=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "path": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hidrive/latest/actions/delete-mail-upload?${params}`, {
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
| `path` | string | yes | Mail upload path to delete. |
| `pid` | string | no | Mail upload public ID to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean | True when HiDrive returns a successful no-content mail upload delete response. |

## Native endpoint

Through the native HiDrive API, this operation is `DELETE /mailupload` (base URL `https://api.hidrive.strato.com/2.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-mail-upload.md) for the provider-specific parameters and requirements.

