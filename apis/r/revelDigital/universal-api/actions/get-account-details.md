# Revel Digital: Get Account Details



```
GET https://connect.mindcloud.co/v1/universal/revelDigital/latest/actions/get-account-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Revel Digital `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/revelDigital/latest/actions/get-account-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/revelDigital/latest/actions/get-account-details?${params}`, {
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
      "address_1": "string",
      "address_2": "string",
      "business_name": "Ava Chen",
      "city": "string",
      "country": "string",
      "created_on": "string",
      "fax": "string",
      "id": "string",
      "logo_url": "https://example.com",
      "name": "Ava Chen",
      "phone": "string",
      "postal_code": "string",
      "primary_contact_id": "string",
      "secondary_contact_id": "string",
      "state": "string",
      "tags": "string",
      "timeZone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address_1` | string |  |
| `address_2` | string |  |
| `business_name` | string |  |
| `city` | string |  |
| `country` | string |  |
| `created_on` | string |  |
| `fax` | string |  |
| `id` | string |  |
| `logo_url` | string |  |
| `name` | string |  |
| `phone` | string |  |
| `postal_code` | string |  |
| `primary_contact_id` | string |  |
| `secondary_contact_id` | string |  |
| `state` | string |  |
| `tags` | string |  |
| `timeZone` | string |  |

## Native endpoint

Through the native Revel Digital API, this operation is `GET /account` (base URL `https://api.reveldigital.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account-details.md) for the provider-specific parameters and requirements.

