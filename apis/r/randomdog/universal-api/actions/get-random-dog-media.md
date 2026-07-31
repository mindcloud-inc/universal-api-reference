# random.dog: Get Random Dog Media



```
GET https://connect.mindcloud.co/v1/universal/randomdog/latest/actions/get-random-dog-media
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a random.dog `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/randomdog/latest/actions/get-random-dog-media?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/randomdog/latest/actions/get-random-dog-media?${params}`, {
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
| `filter` | string | no | Comma-separated media file extensions to exclude. |
| `include` | string | no | Comma-separated media file extensions to include. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "fileSizeBytes": 1,
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fileSizeBytes` | number | Size of the returned dog media file in bytes. |
| `url` | string | Direct URL of the returned random dog media file. |

## Native endpoint

Through the native random.dog API, this operation is `GET /woof.json` (base URL `https://random.dog`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-random-dog-media.md) for the provider-specific parameters and requirements.

