# CRM in Cloud: Get new lead instance

Retrieves a new lead template from CRM in Cloud.

```
GET https://connect.mindcloud.co/v1/universal/cRMInCloud/latest/actions/get-new-lead-instance
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CRM in Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cRMInCloud/latest/actions/get-new-lead-instance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cRMInCloud/latest/actions/get-new-lead-instance?${params}`, {
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
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": 1,
      "lastName": "Chen",
      "phone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `companyName` | string |  |
| `email` | string |  |
| `firstName` | string |  |
| `id` | number |  |
| `lastName` | string |  |
| `phone` | string |  |

## Native endpoint

Through the native CRM in Cloud API, this operation is `GET /Lead/GetNewInstance` (base URL `https://app.crmincloud.it/api/latest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-new-lead-instance.md) for the provider-specific parameters and requirements.

