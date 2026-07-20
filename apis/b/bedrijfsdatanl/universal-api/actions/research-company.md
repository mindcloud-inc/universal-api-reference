# Bedrijfsdata.nl: Research Company



```
GET https://connect.mindcloud.co/v1/universal/bedrijfsdatanl/latest/actions/research-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bedrijfsdata.nl `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bedrijfsdatanl/latest/actions/research-company?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bedrijfsdatanl/latest/actions/research-company?${params}`, {
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
| `q` | string | no | Research query, company name, domain, or identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "brokenMessages": [
        "string"
      ],
      "creditsUsed": 1,
      "creditsUsedMonth": 1,
      "monthlyCredits": 1,
      "product": "string",
      "status": "string",
      "summary": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `brokenMessages[]` | string |  |
| `creditsUsed` | number |  |
| `creditsUsedMonth` | number |  |
| `monthlyCredits` | number |  |
| `product` | string |  |
| `status` | string |  |
| `summary` | string |  |

## Native endpoint

Through the native Bedrijfsdata.nl API, this operation is `GET /llm` (base URL `https://fapi.bedrijfsdata.nl/v1.2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/research-company.md) for the provider-specific parameters and requirements.

