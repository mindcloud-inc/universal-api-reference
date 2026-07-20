# Coresignal: Enrich Multi-source Company

Enriches a multi-source company in Coresignal.

```
POST https://connect.mindcloud.co/v1/universal/coresignal/latest/actions/enrich-multi-source-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Coresignal `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/coresignal/latest/actions/enrich-multi-source-company" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "website": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/coresignal/latest/actions/enrich-multi-source-company', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "website": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `website` | string | yes | Company website URL to enrich. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "company_name": "Ava Chen",
      "employees_count": 1,
      "hq_country": "string",
      "id": 1,
      "industry": "string",
      "linkedin_url": "https://example.com",
      "website": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `company_name` | string |  |
| `employees_count` | number |  |
| `hq_country` | string |  |
| `id` | number |  |
| `industry` | string |  |
| `linkedin_url` | string |  |
| `website` | string |  |

## Native endpoint

Through the native Coresignal API, this operation is `GET /company_multi_source/enrich` (base URL `https://api.coresignal.com/cdapi/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/enrich-multi-source-company.md) for the provider-specific parameters and requirements.

