# Rachio Smart Hose Timer: Get Current Person Info

Retrieves the current person identifier from Rachio.

```
GET https://connect.mindcloud.co/v1/universal/rachioSmartHoseTimer/latest/actions/get-current-person-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rachio Smart Hose Timer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rachioSmartHoseTimer/latest/actions/get-current-person-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rachioSmartHoseTimer/latest/actions/get-current-person-info?${params}`, {
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
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |

## Native endpoint

Through the native Rachio Smart Hose Timer API, this operation is `GET /public/person/info` (base URL `https://api.rach.io/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-person-info.md) for the provider-specific parameters and requirements.

