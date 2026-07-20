# GTmetrix: Get Account Status

Retrieves your current GTmetrix account status.

```
GET https://connect.mindcloud.co/v1/universal/gTmetrix/latest/actions/get-account-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GTmetrix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gTmetrix/latest/actions/get-account-status?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gTmetrix/latest/actions/get-account-status?${params}`, {
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
      "data": {
        "attributes": {
          "account_pro_analysis_options_access": true,
          "account_pro_locations_access": true,
          "account_type": "string",
          "account_whitelabel_pdf_access": true,
          "api_credits": 1,
          "api_refill": 1,
          "api_refill_amount": 1
        },
        "id": "string",
        "type": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.attributes.account_pro_analysis_options_access` | boolean | Whether PRO analysis options are available. |
| `data.attributes.account_pro_locations_access` | boolean | Whether PRO test locations are available. |
| `data.attributes.account_type` | string | GTmetrix account plan type. |
| `data.attributes.account_whitelabel_pdf_access` | boolean | Whether whitelabel PDF export is available. |
| `data.attributes.api_credits` | number | Remaining API credits on the account. |
| `data.attributes.api_refill` | number | Unix timestamp for the next credit refill check. |
| `data.attributes.api_refill_amount` | number | Credits scheduled to be restored at refill time. |
| `data.id` | string | The authenticated GTmetrix API key identifier. |
| `data.type` | string | JSON:API resource type. |

## Native endpoint

Through the native GTmetrix API, this operation is `GET /status` (base URL `https://gtmetrix.com/api/2.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account-status.md) for the provider-specific parameters and requirements.

