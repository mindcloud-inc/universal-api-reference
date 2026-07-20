# Piloterr: Get Crunchbase Company Info



```
GET https://connect.mindcloud.co/v1/universal/piloterr/latest/actions/get-crunchbase-company-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Piloterr `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/piloterr/latest/actions/get-crunchbase-company-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/piloterr/latest/actions/get-crunchbase-company-info?${params}`, {
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
| `domain` | string | no | Domain for Crunchbase reverse company lookup. |
| `query` | string | no | Crunchbase company name, UUID, or URL. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "companyType": "string",
      "employeeCount": "string",
      "headline": "string",
      "name": "Ava Chen",
      "website": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `companyType` | string |  |
| `employeeCount` | string |  |
| `headline` | string |  |
| `name` | string |  |
| `website` | string |  |

## Native endpoint

Through the native Piloterr API, this operation is `GET /crunchbase/company/info` (base URL `https://api.piloterr.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-crunchbase-company-info.md) for the provider-specific parameters and requirements.

