# CRM in Cloud: Get new company instance

Retrieves a new company template from CRM in Cloud.

```
GET https://connect.mindcloud.co/v1/universal/cRMInCloud/latest/actions/get-new-company-instance
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CRM in Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cRMInCloud/latest/actions/get-new-company-instance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cRMInCloud/latest/actions/get-new-company-instance?${params}`, {
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
      "city": "string",
      "code": "string",
      "companyName": "Ava Chen",
      "description": "string",
      "email": "ava@example.com",
      "id": 1,
      "phone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `city` | string |  |
| `code` | string |  |
| `companyName` | string |  |
| `description` | string |  |
| `email` | string |  |
| `id` | number |  |
| `phone` | string |  |

## Native endpoint

Through the native CRM in Cloud API, this operation is `GET /Company/GetNewInstance` (base URL `https://app.crmincloud.it/api/latest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-new-company-instance.md) for the provider-specific parameters and requirements.

