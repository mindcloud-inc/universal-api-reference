# Priority: Get Company

Retrieves a company from Priority.

```
GET https://connect.mindcloud.co/v1/universal/priority/latest/actions/get-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Priority `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/priority/latest/actions/get-company?connectionId=$CONNECTION_ID&companyName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "companyName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/priority/latest/actions/get-company?${params}`, {
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
| `companyName` | string | yes | Priority company key. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "COMPANYDES": "string",
      "COMPANYNAME": "Ava Chen",
      "COUNTRYNAME": "Ava Chen",
      "EMAIL": "ava@example.com",
      "PHONE": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `COMPANYDES` | string |  |
| `COMPANYNAME` | string |  |
| `COUNTRYNAME` | string |  |
| `EMAIL` | string |  |
| `PHONE` | string |  |

## Native endpoint

Through the native Priority API, this operation is `GET /COMPANIES(COMPANYNAME=':companyName')` (base URL `https://t.eu.priority-connect.online/odata/Priority/tabbtd38.ini/usdemo`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-company.md) for the provider-specific parameters and requirements.

