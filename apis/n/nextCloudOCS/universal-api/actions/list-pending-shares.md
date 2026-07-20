# Next Cloud OCS: List Pending Shares

Retrieves pending shares from Next Cloud OCS.

```
GET https://connect.mindcloud.co/v1/universal/nextCloudOCS/latest/actions/list-pending-shares
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Next Cloud OCS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nextCloudOCS/latest/actions/list-pending-shares?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nextCloudOCS/latest/actions/list-pending-shares?${params}`, {
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
      "data": [
        {}
      ],
      "id": "string",
      "ocs": {},
      "path": "string",
      "shareType": 1,
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |
| `id` | string |  |
| `ocs` | object |  |
| `path` | string |  |
| `shareType` | number |  |
| `url` | string |  |

## Native endpoint

Through the native Next Cloud OCS API, this operation is `GET /ocs/v2.php/apps/files_sharing/api/v1/shares/pending` (base URL `https://demo2.nextcloud.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-pending-shares.md) for the provider-specific parameters and requirements.

