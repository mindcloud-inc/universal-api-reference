# HiDrive: Get Unique Identifier

Retrieves a unique identifier from HiDrive.

```
GET https://connect.mindcloud.co/v1/universal/hidrive/latest/actions/get-unique-identifier
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HiDrive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hidrive/latest/actions/get-unique-identifier?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hidrive/latest/actions/get-unique-identifier?${params}`, {
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
      "unique": "string",
      "unique_mac": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `unique` | string | Unique HiDrive identifier. |
| `unique_mac` | string | Unique MAC value. |

## Native endpoint

Through the native HiDrive API, this operation is `GET /unique` (base URL `https://api.hidrive.strato.com/2.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-unique-identifier.md) for the provider-specific parameters and requirements.

