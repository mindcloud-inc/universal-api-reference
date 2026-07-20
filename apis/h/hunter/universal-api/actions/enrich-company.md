# Hunter: Enrich Company



```
GET https://connect.mindcloud.co/v1/universal/hunter/latest/actions/enrich-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hunter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hunter/latest/actions/enrich-company?connectionId=$CONNECTION_ID&domain=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "domain": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hunter/latest/actions/enrich-company?${params}`, {
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
| `domain` | string | yes | Company domain to enrich. |
| `clearbitFormat` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "category": {},
      "companyType": "string",
      "crunchbase": {},
      "description": "string",
      "domain": "string",
      "domainAliases": [
        "string"
      ],
      "emailProvider": "ava@example.com",
      "facebook": {},
      "foundedYear": 1,
      "fundingRounds": [
        {}
      ],
      "geo": {},
      "id": "string",
      "identifiers": {},
      "indexedAt": "string",
      "instagram": {},
      "legalName": "Ava Chen",
      "linkedin": {},
      "location": "string",
      "logo": "string",
      "metrics": {},
      "name": "Ava Chen",
      "parent": {},
      "phone": "string",
      "site": {},
      "tags": [
        "string"
      ],
      "tech": [
        "string"
      ],
      "techCategories": [
        "string"
      ],
      "ticker": "string",
      "timeZone": "string",
      "twitter": {},
      "type": "string",
      "ultimateParent": {},
      "utcOffset": 1,
      "youtube": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `category` | object |  |
| `companyType` | string |  |
| `crunchbase` | object |  |
| `description` | string |  |
| `domain` | string |  |
| `domainAliases` | array<string> |  |
| `emailProvider` | string |  |
| `facebook` | object |  |
| `foundedYear` | number |  |
| `fundingRounds` | array<object> |  |
| `geo` | object |  |
| `id` | string |  |
| `identifiers` | object |  |
| `indexedAt` | string |  |
| `instagram` | object |  |
| `legalName` | string |  |
| `linkedin` | object |  |
| `location` | string |  |
| `logo` | string |  |
| `metrics` | object |  |
| `name` | string |  |
| `parent` | object |  |
| `phone` | string |  |
| `site` | object |  |
| `tags` | array<string> |  |
| `tech` | array<string> |  |
| `techCategories` | array<string> |  |
| `ticker` | string |  |
| `timeZone` | string |  |
| `twitter` | object |  |
| `type` | string |  |
| `ultimateParent` | object |  |
| `utcOffset` | number |  |
| `youtube` | object |  |

## Native endpoint

Through the native Hunter API, this operation is `GET /companies/find` (base URL `https://api.hunter.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/enrich-company.md) for the provider-specific parameters and requirements.

