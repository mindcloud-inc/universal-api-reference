# Listclean: Get Account Profile

Retrieves account profile details from Listclean.

```
GET https://connect.mindcloud.co/v1/universal/listclean/latest/actions/get-account-profile
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Listclean `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/listclean/latest/actions/get-account-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/listclean/latest/actions/get-account-profile?${params}`, {
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
      "address": "string",
      "billing_address": "string",
      "billing_company_name": "Ava Chen",
      "billing_name": "Ava Chen",
      "city": "string",
      "company_name": "Ava Chen",
      "country": "string",
      "email": "ava@example.com",
      "entered": "string",
      "first_name": "Ava",
      "instance_id": 1,
      "last_name": "Chen",
      "linkedin": "https://example.com",
      "phone_number": "string",
      "skype_id": "string",
      "twitter_handle": "string",
      "username": "Ava Chen",
      "website": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string | Profile address. |
| `billing_address` | string | Billing address. |
| `billing_company_name` | string | Billing company name. |
| `billing_name` | string | Billing name. |
| `city` | string | Profile city. |
| `company_name` | string | Company name. |
| `country` | string | Profile country. |
| `email` | string | Account email. |
| `entered` | string | Account creation timestamp. |
| `first_name` | string | First name. |
| `instance_id` | number | Listclean instance ID. |
| `last_name` | string | Last name. |
| `linkedin` | string | LinkedIn profile. |
| `phone_number` | string | Profile phone number. |
| `skype_id` | string | Skype ID. |
| `twitter_handle` | string | Twitter handle. |
| `username` | string | Account username. |
| `website` | string | Website. |

## Native endpoint

Through the native Listclean API, this operation is `GET /account/profile/` (base URL `https://api.listclean.xyz/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account-profile.md) for the provider-specific parameters and requirements.

