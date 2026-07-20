# Bedrijfsdata.nl: Find Company News



```
GET https://connect.mindcloud.co/v1/universal/bedrijfsdatanl/latest/actions/find-company-news
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bedrijfsdata.nl `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bedrijfsdatanl/latest/actions/find-company-news?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bedrijfsdatanl/latest/actions/find-company-news?${params}`, {
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
| `name` | string | no | Company name used to find news. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "creditsUsed": 1,
      "creditsUsedMonth": 1,
      "found": 1,
      "latest": {},
      "monthlyCredits": 1,
      "name": "Ava Chen",
      "nameSearch": "Ava Chen",
      "product": "string",
      "sq": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `creditsUsed` | number |  |
| `creditsUsedMonth` | number |  |
| `found` | number |  |
| `latest` | object |  |
| `monthlyCredits` | number |  |
| `name` | string |  |
| `nameSearch` | string |  |
| `product` | string |  |
| `sq` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Bedrijfsdata.nl API, this operation is `GET /news` (base URL `https://fapi.bedrijfsdata.nl/v1.2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-company-news.md) for the provider-specific parameters and requirements.

