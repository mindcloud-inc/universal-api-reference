# ipdata.co: Get IP Carrier



```
GET https://connect.mindcloud.co/v1/universal/ipdataco/latest/actions/get-ip-carrier
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ipdata.co `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ipdataco/latest/actions/get-ip-carrier?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ipdataco/latest/actions/get-ip-carrier?${params}`, {
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
| `ip` | string | no | The IP address to look up. Default: `69.78.70.144`. Example: `69.78.70.144`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "mcc": "string",
      "mnc": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `mcc` | string | Mobile country code. |
| `mnc` | string | Mobile network code. |
| `name` | string | Mobile carrier name. |

## Native endpoint

Through the native ipdata.co API, this operation is `GET /:ip/carrier` (base URL `https://api.ipdata.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-ip-carrier.md) for the provider-specific parameters and requirements.

