# Seafile: Get Server Information

Retrieves the current Seafile server information.

```
GET https://connect.mindcloud.co/v1/universal/seafile/latest/actions/get-server-information
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Seafile `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seafile/latest/actions/get-server-information?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seafile/latest/actions/get-server-information?${params}`, {
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
      "encrypted_library_version": 1,
      "features": [
        "string"
      ],
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `encrypted_library_version` | number |  |
| `features` | array<string> |  |
| `version` | string |  |

## Native endpoint

Through the native Seafile API, this operation is `GET https://plus.seafile.com/api2/server-info/` (base URL `https://plus.seafile.com/api2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-server-information.md) for the provider-specific parameters and requirements.

