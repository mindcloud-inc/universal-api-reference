# HiDrive: Get Share Link Info

Retrieves share link information from HiDrive.

```
GET https://connect.mindcloud.co/v1/universal/hidrive/latest/actions/get-share-link-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HiDrive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hidrive/latest/actions/get-share-link-info?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hidrive/latest/actions/get-share-link-info?${params}`, {
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
| `id` | string | yes | Public share link ID to inspect. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "has_password": true,
      "id": "string",
      "logo": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `has_password` | boolean | Whether the share link is password protected. |
| `id` | string | Share link ID. |
| `logo` | object | Custom logo information when available. |

## Native endpoint

Through the native HiDrive API, this operation is `GET /sharelink/info` (base URL `https://api.hidrive.strato.com/2.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-share-link-info.md) for the provider-specific parameters and requirements.

