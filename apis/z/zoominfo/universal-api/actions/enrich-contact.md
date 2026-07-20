# Zoominfo: Enrich Contact

Enriches a contact with ZoomInfo data.

```
GET https://connect.mindcloud.co/v1/universal/zoominfo/latest/actions/enrich-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoominfo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zoominfo/latest/actions/enrich-contact?connectionId=$CONNECTION_ID&matchPersonInput%5B%5D=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "matchPersonInput[]": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zoominfo/latest/actions/enrich-contact?${params}`, {
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
| `matchPersonInput[]` | array<object> | yes | Array of contact match objects. Each object can include fields such as personId, fullName, firstName, lastName, emailAddress, phone, companyId, or companyName. |
| `outputFields[]` | array<string> | no | Array of response field names to return. Accepts multiple values as an array. Default: `["mobilePhone","phone","id","companyId"]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "company": {
        "id": 1
      },
      "id": 1,
      "mobilePhone": "string",
      "phone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `company.id` | number |  |
| `id` | number |  |
| `mobilePhone` | string |  |
| `phone` | string |  |

## Native endpoint

Through the native Zoominfo API, this operation is `POST enrich/contact` (base URL `https://api.zoominfo.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/enrich-contact.md) for the provider-specific parameters and requirements.

