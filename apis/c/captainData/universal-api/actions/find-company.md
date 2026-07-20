# Captain Data: Find Company

Finds a company in Captain Data by company name.

```
GET https://connect.mindcloud.co/v1/universal/captainData/latest/actions/find-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Captain Data `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/captainData/latest/actions/find-company?connectionId=$CONNECTION_ID&companyName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "companyName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/captainData/latest/actions/find-company?${params}`, {
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
| `companyName` | string | yes | Company name to resolve to a Captain Data company UID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "li_company_id": "string",
      "li_company_url": "https://example.com",
      "uid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `li_company_id` | string |  |
| `li_company_url` | string |  |
| `uid` | string |  |

## Native endpoint

Through the native Captain Data API, this operation is `GET /companies/find` (base URL `https://api.captaindata.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-company.md) for the provider-specific parameters and requirements.

