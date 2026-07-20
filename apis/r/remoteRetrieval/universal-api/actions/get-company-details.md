# Remote Retrieval: Get Company Details

Retrieves company details from Remote Retrieval.

```
GET https://connect.mindcloud.co/v1/universal/remoteRetrieval/latest/actions/get-company-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Remote Retrieval `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/remoteRetrieval/latest/actions/get-company-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/remoteRetrieval/latest/actions/get-company-details?${params}`, {
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
      "city": "string",
      "company_email": "ava@example.com",
      "company_name": "Ava Chen",
      "created_date": "string",
      "state": "string",
      "zip": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address_1` | string | Primary address line. |
| `address_2` | string | Secondary address line. |
| `city` | string | Company city. |
| `company_email` | string | Company email on the Remote Retrieval account. |
| `company_name` | string | Company name on the Remote Retrieval account. |
| `created_date` | string | Account creation date returned by Remote Retrieval. |
| `state` | string | Company state or province. |
| `zip` | string | Company postal code. |

## Native endpoint

Through the native Remote Retrieval API, this operation is `GET /api/v1/company-details` (base URL `https://www.remoteretrieval.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-company-details.md) for the provider-specific parameters and requirements.

