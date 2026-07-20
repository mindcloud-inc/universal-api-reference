# Cursion: Delete Site

Deletes an existing site from Cursion.

```
DELETE https://connect.mindcloud.co/v1/universal/cursion/latest/actions/delete-site
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cursion `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/cursion/latest/actions/delete-site?connectionId=$CONNECTION_ID&siteId=c38b0fd4-c255-4e22-bb8e-279eed7b6a64" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "siteId": "c38b0fd4-c255-4e22-bb8e-279eed7b6a64"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cursion/latest/actions/delete-site?${params}`, {
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
| `siteId` | string | yes | The site identifier. Default: `c38b0fd4-c255-4e22-bb8e-279eed7b6a64`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |

## Native endpoint

Through the native Cursion API, this operation is `DELETE /site/{{siteId}}` (base URL `https://api.cursion.dev/v1/ops`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-site.md) for the provider-specific parameters and requirements.

