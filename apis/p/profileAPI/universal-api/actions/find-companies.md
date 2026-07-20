# profileAPI: Find Companies

Finds companies in profileAPI by filter criteria.

```
GET https://connect.mindcloud.co/v1/universal/profileAPI/latest/actions/find-companies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a profileAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/profileAPI/latest/actions/find-companies?connectionId=$CONNECTION_ID&filters=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "filters": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/profileAPI/latest/actions/find-companies?${params}`, {
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
| `filters` | object | yes | Filter groups containing all/any filter arrays. Example: `[object Object]`. |
| `limit` | number | no | Maximum number of companies to return. Official docs list default 10 and maximum 1000 for company search. Default: `10`. Example: `100`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "angellistUrl": "https://example.com",
      "crunchbaseUrl": "https://example.com",
      "facebookUrl": "https://example.com",
      "githubUrl": "https://example.com",
      "headcount": 1,
      "headquartersCountryCodes": [
        "string"
      ],
      "headquartersWorldRegions": [
        "string"
      ],
      "id": "string",
      "linkedInId": "https://example.com",
      "linkedInUrl": "https://example.com",
      "logoUrl": "https://example.com",
      "name": "Ava Chen",
      "signals": [
        "string"
      ],
      "stockSymbol": "string",
      "traits": [
        {
          "isActive": true,
          "key": "string"
        }
      ],
      "unitedStatesHeadquartersCities": [
        "string"
      ],
      "unitedStatesHeadquartersRegions": [
        "string"
      ],
      "unitedStatesHeadquartersStateCodes": [
        "string"
      ],
      "website": "string",
      "worldHeadquartersRegions": [
        "string"
      ],
      "xUrl": "https://example.com",
      "youtubeUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `angellistUrl` | string |  |
| `crunchbaseUrl` | string |  |
| `facebookUrl` | string |  |
| `githubUrl` | string |  |
| `headcount` | number |  |
| `headquartersCountryCodes[]` | string |  |
| `headquartersWorldRegions[]` | string |  |
| `id` | string |  |
| `linkedInId` | string |  |
| `linkedInUrl` | string |  |
| `logoUrl` | string |  |
| `name` | string |  |
| `signals[]` | string |  |
| `stockSymbol` | string |  |
| `traits[].isActive` | boolean |  |
| `traits[].key` | string |  |
| `unitedStatesHeadquartersCities[]` | string |  |
| `unitedStatesHeadquartersRegions[]` | string |  |
| `unitedStatesHeadquartersStateCodes[]` | string |  |
| `website` | string |  |
| `worldHeadquartersRegions[]` | string |  |
| `xUrl` | string |  |
| `youtubeUrl` | string |  |

## Native endpoint

Through the native profileAPI API, this operation is `POST /companies/find` (base URL `https://api.profileapi.com/2024-03-01`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-companies.md) for the provider-specific parameters and requirements.

