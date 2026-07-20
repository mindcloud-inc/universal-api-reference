# SMSup: Request HLR Lookup



```
GET https://connect.mindcloud.co/v1/universal/sMSup/latest/actions/request-hlr-lookup
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SMSup `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sMSup/latest/actions/request-hlr-lookup?connectionId=$CONNECTION_ID&msisdn=34666666667" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "msisdn": "34666666667"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sMSup/latest/actions/request-hlr-lookup?${params}`, {
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
| `msisdn` | string | yes | Mobile number in international format. Example: `34666666667`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "mccmnc": "string",
      "msisdn": "string",
      "originalNetwork": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `mccmnc` | string |  |
| `msisdn` | string |  |
| `originalNetwork` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native SMSup API, this operation is `POST /api/hlr/request` (base URL `https://api.gateway360.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/request-hlr-lookup.md) for the provider-specific parameters and requirements.

