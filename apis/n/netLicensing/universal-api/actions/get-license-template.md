# NetLicensing: Get License Template

Retrieves a license template from NetLicensing.

```
GET https://connect.mindcloud.co/v1/universal/netLicensing/latest/actions/get-license-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NetLicensing `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/netLicensing/latest/actions/get-license-template?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/netLicensing/latest/actions/get-license-template?${params}`, {
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
      "active": "string",
      "licenseType": "string",
      "lists": {},
      "name": "Ava Chen",
      "number": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | string |  |
| `licenseType` | string |  |
| `lists` | object |  |
| `name` | string |  |
| `number` | string |  |
| `type` | string |  |

## Native endpoint

Through the native NetLicensing API, this operation is `GET /licensetemplate/{licenseTemplateNumber}` (base URL `https://go.netlicensing.io/core/v2/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-license-template.md) for the provider-specific parameters and requirements.

