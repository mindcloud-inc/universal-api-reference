# HiDrive: Get Features

Retrieves feature information from HiDrive.

```
GET https://connect.mindcloud.co/v1/universal/hidrive/latest/actions/get-features
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HiDrive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hidrive/latest/actions/get-features?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hidrive/latest/actions/get-features?${params}`, {
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
| `fields` | string | no | Comma-separated feature fields to include. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "mailupload_enabled": true,
      "quota": 1,
      "share_edit": true,
      "share_enabled": true,
      "share_ttl": 1,
      "sharelink_password": true,
      "shareupload_enabled": true,
      "shareupload_ttl": 1,
      "snapshot_schedule_type": "string",
      "snapshot_ttl": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `mailupload_enabled` | boolean | Whether mail-upload capability is enabled. |
| `quota` | number | Available quota/feature quota value. |
| `share_edit` | boolean | Whether share editing is available. |
| `share_enabled` | boolean | Whether share capability is enabled. |
| `share_ttl` | number | Share time-to-live setting. |
| `sharelink_password` | boolean | Whether share-link passwords are supported. |
| `shareupload_enabled` | boolean | Whether share-upload capability is enabled. |
| `shareupload_ttl` | number | Share-upload time-to-live setting. |
| `snapshot_schedule_type` | string | Snapshot schedule type. |
| `snapshot_ttl` | number | Snapshot time-to-live setting. |

## Native endpoint

Through the native HiDrive API, this operation is `GET /features` (base URL `https://api.hidrive.strato.com/2.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-features.md) for the provider-specific parameters and requirements.

