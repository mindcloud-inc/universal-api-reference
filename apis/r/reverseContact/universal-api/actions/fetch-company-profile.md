# Reverse Contact: Fetch Company Profile



```
GET https://connect.mindcloud.co/v1/universal/reverseContact/latest/actions/fetch-company-profile
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reverse Contact `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reverseContact/latest/actions/fetch-company-profile?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/reverseContact/latest/actions/fetch-company-profile?${params}`, {
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
| `url` | string | yes | Public Social company URL to fetch. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "backgroundUrl": "https://example.com",
      "description": "string",
      "employeeCount": 1,
      "employeeCountRange": {
        "end": 1,
        "start": 1
      },
      "followerCount": 1,
      "foundedOn": {
        "year": 1
      },
      "headquarter": {
        "city": "string",
        "country": "string",
        "geographicArea": "string",
        "postalCode": "string"
      },
      "industry": "string",
      "linkedInId": "https://example.com",
      "linkedInUrl": "https://example.com",
      "logo": "string",
      "name": "Ava Chen",
      "phone": "string",
      "specialities": [
        "string"
      ],
      "tagline": "string",
      "universalName": "Ava Chen",
      "websiteUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `backgroundUrl` | string |  |
| `description` | string |  |
| `employeeCount` | number |  |
| `employeeCountRange.end` | number |  |
| `employeeCountRange.start` | number |  |
| `followerCount` | number |  |
| `foundedOn.year` | number |  |
| `headquarter.city` | string |  |
| `headquarter.country` | string |  |
| `headquarter.geographicArea` | string |  |
| `headquarter.postalCode` | string |  |
| `industry` | string |  |
| `linkedInId` | string |  |
| `linkedInUrl` | string |  |
| `logo` | string |  |
| `name` | string |  |
| `phone` | string |  |
| `specialities` | array<string> |  |
| `tagline` | string |  |
| `universalName` | string |  |
| `websiteUrl` | string |  |

## Native endpoint

Through the native Reverse Contact API, this operation is `POST /v2/fetch/companies` (base URL `https://api.reversecontact.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/fetch-company-profile.md) for the provider-specific parameters and requirements.

