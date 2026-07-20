# Listclean: Update Account Profile

Updates account profile details in Listclean.

```
PUT https://connect.mindcloud.co/v1/universal/listclean/latest/actions/update-account-profile
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Listclean `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/listclean/latest/actions/update-account-profile" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/listclean/latest/actions/update-account-profile', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `address` | string | no | Profile address. |
| `billing_address` | string | no | Billing address. |
| `billing_company_name` | string | no | Billing company name. |
| `billing_name` | string | no | Billing name. |
| `city` | string | no | Profile city. |
| `company_name` | string | no | Company name. |
| `country` | string | no | Profile country. |
| `linkedin` | string | no | LinkedIn profile. |
| `name` | string | no | First name of the user. |
| `phone_number` | string | no | Profile phone number. |
| `skype_id` | string | no | Skype ID. |
| `twitter_handle` | string | no | Twitter handle. |
| `website` | string | no | Website. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "error_code": 1,
      "message": "string",
      "success": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `error_code` | number | Provider error code. |
| `message` | string | Update result message. |
| `success` | number | Provider success flag. |

## Native endpoint

Through the native Listclean API, this operation is `POST /account/profile/` (base URL `https://api.listclean.xyz/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-account-profile.md) for the provider-specific parameters and requirements.

