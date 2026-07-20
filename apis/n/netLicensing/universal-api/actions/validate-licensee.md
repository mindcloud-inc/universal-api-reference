# NetLicensing: Validate Licensee

Retrieves license validation results from NetLicensing.

```
GET https://connect.mindcloud.co/v1/universal/netLicensing/latest/actions/validate-licensee
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NetLicensing `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/netLicensing/latest/actions/validate-licensee?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/netLicensing/latest/actions/validate-licensee?${params}`, {
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
      "licensingModel": "string",
      "lists": {},
      "productModuleName": "Ava Chen",
      "productModuleNumber": "string",
      "type": "string",
      "valid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `licensingModel` | string |  |
| `lists` | object |  |
| `productModuleName` | string |  |
| `productModuleNumber` | string |  |
| `type` | string |  |
| `valid` | string |  |

## Native endpoint

Through the native NetLicensing API, this operation is `POST /licensee/{licenseeNumber}/validate` (base URL `https://go.netlicensing.io/core/v2/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-licensee.md) for the provider-specific parameters and requirements.

