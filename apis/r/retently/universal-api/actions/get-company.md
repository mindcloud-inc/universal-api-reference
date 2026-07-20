# Retently: Get Company

Retrieves a company from Retently by ID or domain.

```
GET https://connect.mindcloud.co/v1/universal/retently/latest/actions/get-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Retently `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/retently/latest/actions/get-company?connectionId=$CONNECTION_ID&companyIdOrDomain=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "companyIdOrDomain": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/retently/latest/actions/get-company?${params}`, {
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
| `companyIdOrDomain` | string | yes | Company ID or domain. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "companyName": "Ava Chen",
      "contactsCount": 1,
      "createdDate": "string",
      "cxMetrics": {},
      "domain": "string",
      "id": "string",
      "industryName": "Ava Chen",
      "tags": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `companyName` | string |  |
| `contactsCount` | number |  |
| `createdDate` | string |  |
| `cxMetrics` | object |  |
| `domain` | string |  |
| `id` | string |  |
| `industryName` | string |  |
| `tags` | array<string> |  |

## Native endpoint

Through the native Retently API, this operation is `GET /api/v2/companies/:companyIdOrDomain` (base URL `https://app.retently.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-company.md) for the provider-specific parameters and requirements.

