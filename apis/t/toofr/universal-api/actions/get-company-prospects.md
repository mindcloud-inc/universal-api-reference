# Toofr: Get Company Prospects

Retrieves prospects for a company from Toofr.

```
GET https://connect.mindcloud.co/v1/universal/toofr/latest/actions/get-company-prospects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Toofr `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/toofr/latest/actions/get-company-prospects?connectionId=$CONNECTION_ID&companyName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "companyName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/toofr/latest/actions/get-company-prospects?${params}`, {
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
| `companyName` | string | yes | Company name to retrieve prospects for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "company": "string",
      "confidence": 1,
      "email_address": "ava@example.com",
      "first_name": "Ava",
      "last_name": "Chen",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `company` | string |  |
| `confidence` | number |  |
| `email_address` | string |  |
| `first_name` | string |  |
| `last_name` | string |  |
| `title` | string |  |

## Native endpoint

Through the native Toofr API, this operation is `GET /get_prospects` (base URL `https://www.findemails.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-company-prospects.md) for the provider-specific parameters and requirements.

