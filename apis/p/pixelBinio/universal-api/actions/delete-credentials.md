# PixelBin.io: Delete Transformation Module Credentials

Deletes transformation module credentials from PixelBin.io.

```
DELETE https://connect.mindcloud.co/v1/universal/pixelBinio/latest/actions/delete-credentials
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PixelBin.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/pixelBinio/latest/actions/delete-credentials?connectionId=$CONNECTION_ID&pluginId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "pluginId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pixelBinio/latest/actions/delete-credentials?${params}`, {
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
| `pluginId` | string | yes | Transformation module identifier whose credentials you want to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "credentials": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `credentials` | object | Transformation module credentials object associated with the deleted configuration. |

## Native endpoint

Through the native PixelBin.io API, this operation is `DELETE /service/platform/assets/v1.0/credentials/:pluginId` (base URL `https://api.pixelbin.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-credentials.md) for the provider-specific parameters and requirements.

