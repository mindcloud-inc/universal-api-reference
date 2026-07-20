# Dolibarr: Get Status

Retrieves status information for the Dolibarr instance.

```
GET https://connect.mindcloud.co/v1/universal/dolibarr/latest/actions/get-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dolibarr `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dolibarr/latest/actions/get-status?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dolibarr/latest/actions/get-status?${params}`, {
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
      "success": {
        "access_locked": "string",
        "code": 1,
        "dolibarr_version": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | object | Dolibarr status response envelope. |
| `success.access_locked` | string | Dolibarr access lock flag. |
| `success.code` | number | HTTP-like status code returned by Dolibarr. |
| `success.dolibarr_version` | string | Dolibarr server version. |

## Native endpoint

Through the native Dolibarr API, this operation is `GET /status` (base URL `https://mindcloud-dolibarr-0421.with7.dolicloud.com/api/index.php`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-status.md) for the provider-specific parameters and requirements.

