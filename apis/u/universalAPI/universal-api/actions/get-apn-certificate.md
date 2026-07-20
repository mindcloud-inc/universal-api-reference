# Universal API: Get APN Certificate

Retrieves an APN certificate from Universal API.

```
GET https://connect.mindcloud.co/v1/universal/universalAPI/latest/actions/get-apn-certificate
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Universal API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/universalAPI/latest/actions/get-apn-certificate?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/universalAPI/latest/actions/get-apn-certificate?${params}`, {
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
      "expiresAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `expiresAt` | date |  |
| `id` | string |  |
| `name` | string |  |

## Native endpoint

Through the native Universal API API, this operation is `GET /api/mdm/apn-cert` (base URL `https://api.prod.universalapi.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-apn-certificate.md) for the provider-specific parameters and requirements.

