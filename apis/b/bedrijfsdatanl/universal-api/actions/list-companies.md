# Bedrijfsdata.nl: List Companies



```
GET https://connect.mindcloud.co/v1/universal/bedrijfsdatanl/latest/actions/list-companies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bedrijfsdata.nl `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bedrijfsdatanl/latest/actions/list-companies?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bedrijfsdatanl/latest/actions/list-companies?${params}`, {
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
| `search` | string | no | Optional search query for company discovery. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "companies": [
        {
          "address": "string",
          "addressid": "string",
          "apps": [
            "string"
          ],
          "appsCat": [
            "string"
          ],
          "appsCms": [
            "string"
          ],
          "appsTagManagers": [
            "string"
          ],
          "bagAddressid": "string",
          "bagBouwjaar": 1,
          "bagGebruiksdoel": "string",
          "bagOppervlakte": 1,
          "bagOppervlakteAvg": 1,
          "bagPndId": "string",
          "bingId": [
            "string"
          ],
          "ch": "string",
          "city": "string",
          "coc": "string",
          "country": "string",
          "countryCode": "string",
          "dataExists": [
            "string"
          ],
          "description": "string",
          "domain": "string",
          "email": "ava@example.com",
          "employees": 1,
          "employeesRange": 1,
          "facebookFollowers": 1,
          "facebookId": 1,
          "facebookLink": "https://example.com",
          "facebookRating": [
            "string"
          ],
          "facebookReviews": [
            "string"
          ],
          "fastRank": 1,
          "fd": "string",
          "founded": 1,
          "fullProfile": "string",
          "geo": "string",
          "googleId": [
            "string"
          ],
          "id": "string",
          "imageUrl": [
            "https://example.com"
          ],
          "imageUrlMain": [
            "https://example.com"
          ],
          "imageUrls": [
            "https://example.com"
          ],
          "industry": [
            "string"
          ],
          "industrySection": [
            "string"
          ],
          "introduction": "string",
          "introductionEn": [
            "string"
          ],
          "introductionNl": [
            "string"
          ],
          "isic": [
            "string"
          ],
          "keywordEn": [
            "string"
          ],
          "keywordNl": [
            "string"
          ],
          "keywords": [
            "string"
          ],
          "lang": [
            "string"
          ],
          "linkedBy": [
            "https://example.com"
          ],
          "linkedCount": 1,
          "linkedinIndustryShort": [
            "https://example.com"
          ],
          "linkedKeyword": [
            "https://example.com"
          ],
          "linkedRank": 1,
          "mentionedBy": [
            "string"
          ],
          "municipality": "string",
          "naceIndustry": [
            "string"
          ],
          "naics": [
            "string"
          ],
          "naicsIndustry": [
            "string"
          ],
          "name": "Ava Chen",
          "names": [
            "Ava Chen"
          ],
          "officeType": "string",
          "orgtype": "string",
          "phone": "string",
          "phoneInternational": "string",
          "postcode": "string",
          "province": "string",
          "provinceLocal": "string",
          "rank": 1,
          "rating": 1,
          "registerId": [
            "string"
          ],
          "relatedUrlsList": [
            "https://example.com"
          ],
          "revenue": 1,
          "revenueRange": 1,
          "reviews": 1,
          "sbi": [
            "string"
          ],
          "sbi2008": [
            "string"
          ],
          "sbi2025": [
            "string"
          ],
          "sbiMain": [
            "string"
          ],
          "socialExists": [
            "string"
          ],
          "socialInteractions": 1,
          "ultimateParentCocs": [
            "string"
          ],
          "url": "https://example.com",
          "ussic8": [
            "string"
          ],
          "ussic8Industry": [
            "string"
          ],
          "vat": "string"
        }
      ],
      "creditsUsed": 1,
      "creditsUsedMonth": 1,
      "found": 1,
      "monthlyCredits": 1,
      "product": "string",
      "q": "string",
      "qid": 1,
      "status": "string",
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `companies[].address` | string |  |
| `companies[].addressid` | string |  |
| `companies[].apps[]` | string |  |
| `companies[].appsCat[]` | string |  |
| `companies[].appsCms[]` | string |  |
| `companies[].appsTagManagers[]` | string |  |
| `companies[].bagAddressid` | string |  |
| `companies[].bagBouwjaar` | number |  |
| `companies[].bagGebruiksdoel` | string |  |
| `companies[].bagOppervlakte` | number |  |
| `companies[].bagOppervlakteAvg` | number |  |
| `companies[].bagPndId` | string |  |
| `companies[].bingId[]` | string |  |
| `companies[].ch` | string |  |
| `companies[].city` | string |  |
| `companies[].coc` | string |  |
| `companies[].country` | string |  |
| `companies[].countryCode` | string |  |
| `companies[].dataExists[]` | string |  |
| `companies[].description` | string |  |
| `companies[].domain` | string |  |
| `companies[].email` | string |  |
| `companies[].employees` | number |  |
| `companies[].employeesRange` | number |  |
| `companies[].facebookFollowers` | number |  |
| `companies[].facebookId` | number |  |
| `companies[].facebookLink` | string |  |
| `companies[].facebookRating[]` | string |  |
| `companies[].facebookReviews[]` | string |  |
| `companies[].fastRank` | number |  |
| `companies[].fd` | string |  |
| `companies[].founded` | number |  |
| `companies[].fullProfile` | string |  |
| `companies[].geo` | string |  |
| `companies[].googleId[]` | string |  |
| `companies[].id` | string |  |
| `companies[].imageUrl[]` | string |  |
| `companies[].imageUrlMain[]` | string |  |
| `companies[].imageUrls[]` | string |  |
| `companies[].industry[]` | string |  |
| `companies[].industrySection[]` | string |  |
| `companies[].introduction` | string |  |
| `companies[].introductionEn[]` | string |  |
| `companies[].introductionNl[]` | string |  |
| `companies[].isic[]` | string |  |
| `companies[].keywordEn[]` | string |  |
| `companies[].keywordNl[]` | string |  |
| `companies[].keywords[]` | string |  |
| `companies[].lang[]` | string |  |
| `companies[].linkedBy[]` | string |  |
| `companies[].linkedCount` | number |  |
| `companies[].linkedinIndustryShort[]` | string |  |
| `companies[].linkedKeyword[]` | string |  |
| `companies[].linkedRank` | number |  |
| `companies[].mentionedBy[]` | string |  |
| `companies[].municipality` | string |  |
| `companies[].naceIndustry[]` | string |  |
| `companies[].naics[]` | string |  |
| `companies[].naicsIndustry[]` | string |  |
| `companies[].name` | string |  |
| `companies[].names[]` | string |  |
| `companies[].officeType` | string |  |
| `companies[].orgtype` | string |  |
| `companies[].phone` | string |  |
| `companies[].phoneInternational` | string |  |
| `companies[].postcode` | string |  |
| `companies[].province` | string |  |
| `companies[].provinceLocal` | string |  |
| `companies[].rank` | number |  |
| `companies[].rating` | number |  |
| `companies[].registerId[]` | string |  |
| `companies[].relatedUrlsList[]` | string |  |
| `companies[].revenue` | number |  |
| `companies[].revenueRange` | number |  |
| `companies[].reviews` | number |  |
| `companies[].sbi[]` | string |  |
| `companies[].sbi2008[]` | string |  |
| `companies[].sbi2025[]` | string |  |
| `companies[].sbiMain[]` | string |  |
| `companies[].socialExists[]` | string |  |
| `companies[].socialInteractions` | number |  |
| `companies[].ultimateParentCocs[]` | string |  |
| `companies[].url` | string |  |
| `companies[].ussic8[]` | string |  |
| `companies[].ussic8Industry[]` | string |  |
| `companies[].vat` | string |  |
| `creditsUsed` | number |  |
| `creditsUsedMonth` | number |  |
| `found` | number |  |
| `monthlyCredits` | number |  |
| `product` | string |  |
| `q` | string |  |
| `qid` | number |  |
| `status` | string |  |
| `total` | number |  |

## Native endpoint

Through the native Bedrijfsdata.nl API, this operation is `GET /companies` (base URL `https://fapi.bedrijfsdata.nl/v1.2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-companies.md) for the provider-specific parameters and requirements.

