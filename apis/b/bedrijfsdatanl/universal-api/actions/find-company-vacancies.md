# Bedrijfsdata.nl: Find Company Vacancies



```
GET https://connect.mindcloud.co/v1/universal/bedrijfsdatanl/latest/actions/find-company-vacancies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bedrijfsdata.nl `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bedrijfsdatanl/latest/actions/find-company-vacancies?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bedrijfsdatanl/latest/actions/find-company-vacancies?${params}`, {
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
| `coc` | string | no | Dutch Chamber of Commerce number used to find vacancies. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ago": 1,
      "creditsUsed": 1,
      "creditsUsedMonth": 1,
      "found": 1,
      "latest": 1,
      "monthlyCredits": 1,
      "product": "string",
      "status": "string",
      "vacancies": [
        {
          "active": 1,
          "coc": "string",
          "company": "string",
          "date": "2026-05-07T12:00:00.000Z",
          "domain": "string",
          "id": "string",
          "logo": "string",
          "rank": 1,
          "time": "2026-05-07T12:00:00.000Z",
          "title": "string",
          "url": "https://example.com"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ago` | number |  |
| `creditsUsed` | number |  |
| `creditsUsedMonth` | number |  |
| `found` | number |  |
| `latest` | number |  |
| `monthlyCredits` | number |  |
| `product` | string |  |
| `status` | string |  |
| `vacancies[].active` | number |  |
| `vacancies[].coc` | string |  |
| `vacancies[].company` | string |  |
| `vacancies[].date` | date |  |
| `vacancies[].domain` | string |  |
| `vacancies[].id` | string |  |
| `vacancies[].logo` | string |  |
| `vacancies[].rank` | number |  |
| `vacancies[].time` | date |  |
| `vacancies[].title` | string |  |
| `vacancies[].url` | string |  |

## Native endpoint

Through the native Bedrijfsdata.nl API, this operation is `GET /vacancies` (base URL `https://fapi.bedrijfsdata.nl/v1.2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-company-vacancies.md) for the provider-specific parameters and requirements.

