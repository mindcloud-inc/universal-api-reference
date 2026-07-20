# Codemagic: Get Shorebird Metadata

Retrieves Shorebird integration information from Codemagic.

```
GET https://connect.mindcloud.co/v1/universal/codemagic/latest/actions/get-shorebird-metadata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Codemagic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/codemagic/latest/actions/get-shorebird-metadata?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/codemagic/latest/actions/get-shorebird-metadata?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "flutter_versions": [
        "string"
      ],
      "shorebird_version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `flutter_versions` | array<string> |  |
| `shorebird_version` | string |  |

## Native endpoint

Through the native Codemagic API, this operation is `GET /api/v3/meta/shorebird` (base URL `https://codemagic.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-shorebird-metadata.md) for the provider-specific parameters and requirements.

