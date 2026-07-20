# PhantomBuster: Get IP Location

Retrieves IP location details from PhantomBuster.

```
GET https://connect.mindcloud.co/v1/universal/phantomBuster/latest/actions/get-ip-location
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PhantomBuster `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/phantomBuster/latest/actions/get-ip-location?connectionId=$CONNECTION_ID&ip=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ip": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/phantomBuster/latest/actions/get-ip-location?${params}`, {
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
| `ip` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "country": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `country` | string |  |

## Native endpoint

Through the native PhantomBuster API, this operation is `GET /location/ip` (base URL `https://api.phantombuster.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-ip-location.md) for the provider-specific parameters and requirements.

