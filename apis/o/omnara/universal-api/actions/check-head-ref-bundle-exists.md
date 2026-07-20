# Omnara: Check Head Ref Bundle Exists



```
GET https://connect.mindcloud.co/v1/universal/omnara/latest/actions/check-head-ref-bundle-exists
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Omnara `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/omnara/latest/actions/check-head-ref-bundle-exists?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/omnara/latest/actions/check-head-ref-bundle-exists?${params}`, {
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
      "exists": true,
      "storageKey": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `exists` | boolean |  |
| `storageKey` | string |  |

## Native endpoint

Through the native Omnara API, this operation is `POST /api/v1/workspaces/{workspaceId}/sync/head-ref-exists` (base URL `https://api.omnara.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-head-ref-bundle-exists.md) for the provider-specific parameters and requirements.

