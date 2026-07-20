# BunnyCDN: Remove Custom Hostname

Removes a custom hostname from a BunnyCDN pull zone.

```
DELETE https://connect.mindcloud.co/v1/universal/bunnyCDN/latest/actions/remove-custom-hostname
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BunnyCDN `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/bunnyCDN/latest/actions/remove-custom-hostname?connectionId=$CONNECTION_ID&id=string&hostname=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string",
  "hostname": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bunnyCDN/latest/actions/remove-custom-hostname?${params}`, {
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
| `id` | string | yes | The Bunny pull zone ID. |
| `hostname` | string | yes | The hostname that will be removed. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ErrorKey": "string",
      "Field": "string",
      "Message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ErrorKey` | string |  |
| `Field` | string |  |
| `Message` | string |  |

## Native endpoint

Through the native BunnyCDN API, this operation is `DELETE /pullzone/:id/removeHostname` (base URL `https://api.bunny.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-custom-hostname.md) for the provider-specific parameters and requirements.

