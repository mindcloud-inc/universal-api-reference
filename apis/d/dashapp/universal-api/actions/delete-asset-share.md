# Dash.app: Delete Asset Share

Deletes an existing asset share from Dash.app.

```
DELETE https://connect.mindcloud.co/v1/universal/dashapp/latest/actions/delete-asset-share
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dash.app `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/dashapp/latest/actions/delete-asset-share?connectionId=$CONNECTION_ID&id=4517a7ba-a482-4211-b97e-f4256f53fd32" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "4517a7ba-a482-4211-b97e-f4256f53fd32"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dashapp/latest/actions/delete-asset-share?${params}`, {
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
| `id` | string | yes | Default: `4517a7ba-a482-4211-b97e-f4256f53fd32`. Example: `4517a7ba-a482-4211-b97e-f4256f53fd32`. |

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
| `success` | boolean |  |

## Native endpoint

Through the native Dash.app API, this operation is `DELETE /asset-shares/:id` (base URL `https://api-v2.dash.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-asset-share.md) for the provider-specific parameters and requirements.

