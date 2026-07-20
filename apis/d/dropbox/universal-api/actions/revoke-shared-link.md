# Dropbox: Revoke Shared Link

Deletes an existing shared link from Dropbox.

```
DELETE https://connect.mindcloud.co/v1/universal/dropbox/latest/actions/revoke-shared-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dropbox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/dropbox/latest/actions/revoke-shared-link?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fwww.dropbox.com%2Fs%2Fexample%2Fshared-file.txt%3Fdl%3D0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://www.dropbox.com/s/example/shared-file.txt?dl=0"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dropbox/latest/actions/revoke-shared-link?${params}`, {
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
| `url` | string | yes | Example: `https://www.dropbox.com/s/example/shared-file.txt?dl=0`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `url` | string | Official Dropbox SDK docs define this endpoint response as void (empty response body). |

## Native endpoint

Through the native Dropbox API, this operation is `POST /sharing/revoke_shared_link` (base URL `https://api.dropboxapi.com/2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/revoke-shared-link.md) for the provider-specific parameters and requirements.

