# Zoho CRM: Get Organization Details

Retrieves organization details from Zoho CRM.

```
GET https://connect.mindcloud.co/v1/universal/zohoCRM/latest/actions/get-organization-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoCRM/latest/actions/get-organization-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoCRM/latest/actions/get-organization-details?${params}`, {
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
      "companyName": "Ava Chen",
      "countryCode": "string",
      "createdTime": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "id": "string",
      "phone": "string",
      "primaryEmail": "ava@example.com",
      "timeZone": "string",
      "zgid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `companyName` | string |  |
| `countryCode` | string |  |
| `createdTime` | date |  |
| `currency` | string |  |
| `id` | string |  |
| `phone` | string |  |
| `primaryEmail` | string |  |
| `timeZone` | string |  |
| `zgid` | string |  |

## Native endpoint

Through the native Zoho CRM API, this operation is `GET /org` (base URL `{{credentials.accessTokenRequest.api_domain}}/crm/v8`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-organization-details.md) for the provider-specific parameters and requirements.

