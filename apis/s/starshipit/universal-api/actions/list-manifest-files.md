# Starshipit: List Manifest Files



```
GET https://connect.mindcloud.co/v1/universal/starshipit/latest/actions/list-manifest-files
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Starshipit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/starshipit/latest/actions/list-manifest-files?connectionId=$CONNECTION_ID&manifestId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "manifestId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/starshipit/latest/actions/list-manifest-files?${params}`, {
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
| `manifestId` | number | yes | The unique numeric identifier for the manifest |

## Response

```json
{
  "success": true,
  "data": [
    {
      "files": [
        {
          "fileData": "string",
          "fileName": "Ava Chen"
        }
      ],
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `files` | array<object> |  |
| `files[].fileData` | string |  |
| `files[].fileName` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Starshipit API, this operation is `GET /manifests/files/` (base URL `https://api.starshipit.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-manifest-files.md) for the provider-specific parameters and requirements.

