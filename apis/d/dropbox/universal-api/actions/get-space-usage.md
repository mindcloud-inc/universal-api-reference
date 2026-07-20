# Dropbox: Get Space Usage

Retrieves account space usage from Dropbox.

```
GET https://connect.mindcloud.co/v1/universal/dropbox/latest/actions/get-space-usage
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dropbox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dropbox/latest/actions/get-space-usage?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dropbox/latest/actions/get-space-usage?${params}`, {
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
      "allocation": {
        "allocated": 1,
        "tag": "string"
      },
      "used": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allocation.allocated` | number |  |
| `allocation.tag` | string |  |
| `used` | number |  |

## Native endpoint

Through the native Dropbox API, this operation is `POST /users/get_space_usage` (base URL `https://api.dropboxapi.com/2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-space-usage.md) for the provider-specific parameters and requirements.

