# Zoominfo: Enrich Company

Enriches a company with ZoomInfo data.

```
GET https://connect.mindcloud.co/v1/universal/zoominfo/latest/actions/enrich-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoominfo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zoominfo/latest/actions/enrich-company?connectionId=$CONNECTION_ID&matchCompanyInput%5B%5D=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "matchCompanyInput[]": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zoominfo/latest/actions/enrich-company?${params}`, {
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
| `matchCompanyInput[]` | array<object> | yes | Array of company match objects. Each object can include fields such as companyId, companyName, companyWebsite, companyTicker, companyPhone, or companyCountry. |
| `outputFields[]` | array<string> | no | Array of response field names to return. Accepts multiple values as an array. Default: `["id","ticker","name","website","domainList"]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "domainList": [
        "string"
      ],
      "id": 1,
      "name": "Ava Chen",
      "ticker": "string",
      "website": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `domainList` | array<string> |  |
| `id` | number |  |
| `name` | string |  |
| `ticker` | string |  |
| `website` | string |  |

## Native endpoint

Through the native Zoominfo API, this operation is `POST enrich/company` (base URL `https://api.zoominfo.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/enrich-company.md) for the provider-specific parameters and requirements.

