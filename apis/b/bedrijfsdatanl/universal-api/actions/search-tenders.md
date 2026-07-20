# Bedrijfsdata.nl: Search Tenders



```
GET https://connect.mindcloud.co/v1/universal/bedrijfsdatanl/latest/actions/search-tenders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bedrijfsdata.nl `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bedrijfsdatanl/latest/actions/search-tenders?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bedrijfsdatanl/latest/actions/search-tenders?${params}`, {
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
| `q` | string | no | Tender search query. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "creditsUsed": 1,
      "creditsUsedMonth": 1,
      "found": 1,
      "monthlyCredits": 1,
      "product": "string",
      "status": "string",
      "tender": [
        {
          "bt5071Lot": "string",
          "bt5071Procedure": "string",
          "bt5141Lot": "string",
          "bt5141Procedure": "string",
          "buyer": "string",
          "buyerCountry": "string",
          "contractNature": "string",
          "html": "string",
          "id": "string",
          "link": "https://example.com",
          "noticeType": "string",
          "officialLanguage": "string",
          "pdf": "string",
          "placeOfPerformance": "string",
          "procedureType": "string",
          "publicationDate": "2026-05-07T12:00:00.000Z",
          "title": "string"
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
| `creditsUsed` | number |  |
| `creditsUsedMonth` | number |  |
| `found` | number |  |
| `monthlyCredits` | number |  |
| `product` | string |  |
| `status` | string |  |
| `tender[].bt5071Lot` | string |  |
| `tender[].bt5071Procedure` | string |  |
| `tender[].bt5141Lot` | string |  |
| `tender[].bt5141Procedure` | string |  |
| `tender[].buyer` | string |  |
| `tender[].buyerCountry` | string |  |
| `tender[].contractNature` | string |  |
| `tender[].html` | string |  |
| `tender[].id` | string |  |
| `tender[].link` | string |  |
| `tender[].noticeType` | string |  |
| `tender[].officialLanguage` | string |  |
| `tender[].pdf` | string |  |
| `tender[].placeOfPerformance` | string |  |
| `tender[].procedureType` | string |  |
| `tender[].publicationDate` | date |  |
| `tender[].title` | string |  |

## Native endpoint

Through the native Bedrijfsdata.nl API, this operation is `GET /tender` (base URL `https://fapi.bedrijfsdata.nl/v1.2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-tenders.md) for the provider-specific parameters and requirements.

