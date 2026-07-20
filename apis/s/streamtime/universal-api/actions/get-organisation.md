# Streamtime: Get Organisation



```
GET https://connect.mindcloud.co/v1/universal/streamtime/latest/actions/get-organisation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Streamtime `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/streamtime/latest/actions/get-organisation?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/streamtime/latest/actions/get-organisation?${params}`, {
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
      "address": {},
      "country": {},
      "currency": {},
      "domain": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | object | Organisation address |
| `country` | object | Organisation country |
| `currency` | object | Organisation currency |
| `domain` | string | Organisation domain |
| `name` | string | Organisation name |

## Native endpoint

Through the native Streamtime API, this operation is `GET /organisation` (base URL `https://api.streamtime.net/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-organisation.md) for the provider-specific parameters and requirements.

