# Next Cloud OCS: Search Sharees

Finds sharees in Next Cloud OCS.

```
GET https://connect.mindcloud.co/v1/universal/nextCloudOCS/latest/actions/search-sharees
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Next Cloud OCS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nextCloudOCS/latest/actions/search-sharees?connectionId=$CONNECTION_ID&search=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "search": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nextCloudOCS/latest/actions/search-sharees?${params}`, {
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
| `search` | string | yes | Search term for sharee lookup. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "label": "string",
      "shareType": 1,
      "shareWith": "string",
      "value": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `label` | string |  |
| `shareType` | number |  |
| `shareWith` | string |  |
| `value` | object |  |

## Native endpoint

Through the native Next Cloud OCS API, this operation is `GET /ocs/v1.php/apps/files_sharing/api/v1/sharees` (base URL `https://demo2.nextcloud.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-sharees.md) for the provider-specific parameters and requirements.

