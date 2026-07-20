# Cryptolens: Get License Templates

Retrieves license templates from Cryptolens.

```
GET https://connect.mindcloud.co/v1/universal/cryptolens/latest/actions/get-license-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cryptolens `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cryptolens/latest/actions/get-license-templates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cryptolens/latest/actions/get-license-templates?${params}`, {
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
      "id": 1,
      "name": "Ava Chen",
      "parameters": "string",
      "productId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number | Get License Templates response field `id` from Cryptolens docs example. |
| `name` | string | Get License Templates response field `name` from Cryptolens docs example. |
| `parameters` | string | Get License Templates response field `parameters` from Cryptolens docs example. |
| `productId` | number | Get License Templates response field `productId` from Cryptolens docs example. |

## Native endpoint

Through the native Cryptolens API, this operation is `GET /api/licensetemplate/GetLicenseTemplates` (base URL `https://api.cryptolens.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-license-templates.md) for the provider-specific parameters and requirements.

