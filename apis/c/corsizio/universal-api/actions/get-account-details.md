# Corsizio: Get Account Details

Retrieves account details from a Corsizio account.

```
GET https://connect.mindcloud.co/v1/universal/corsizio/latest/actions/get-account-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Corsizio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/corsizio/latest/actions/get-account-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/corsizio/latest/actions/get-account-details?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "ageGroups": [
        {
          "id": "string",
          "label": "string"
        }
      ],
      "alias": "string",
      "categories": [
        {
          "id": "string",
          "label": "string"
        }
      ],
      "contact": {
        "email": "ava@example.com",
        "name": "Ava Chen",
        "phone": "string"
      },
      "created": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "genders": [
        {
          "id": "string",
          "label": "string"
        }
      ],
      "id": "string",
      "levels": [
        {
          "id": "string",
          "label": "string"
        }
      ],
      "locations": [
        {
          "city": "string",
          "country": "string",
          "id": "string",
          "label": "string",
          "name": "Ava Chen",
          "state": "string",
          "street": "string",
          "zip": "string"
        }
      ],
      "name": "Ava Chen",
      "priceRanges": [
        {
          "from": 1,
          "id": "string",
          "label": "string",
          "to": 1,
          "value": "string"
        }
      ],
      "siteUrl": "https://example.com",
      "timeZone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ageGroups[].id` | string |  |
| `ageGroups[].label` | string |  |
| `alias` | string |  |
| `categories[].id` | string |  |
| `categories[].label` | string |  |
| `contact.email` | string |  |
| `contact.name` | string |  |
| `contact.phone` | string |  |
| `created` | date |  |
| `currency` | string |  |
| `genders[].id` | string |  |
| `genders[].label` | string |  |
| `id` | string |  |
| `levels[].id` | string |  |
| `levels[].label` | string |  |
| `locations[].city` | string |  |
| `locations[].country` | string |  |
| `locations[].id` | string |  |
| `locations[].label` | string |  |
| `locations[].name` | string |  |
| `locations[].state` | string |  |
| `locations[].street` | string |  |
| `locations[].zip` | string |  |
| `name` | string |  |
| `priceRanges[].from` | number |  |
| `priceRanges[].id` | string |  |
| `priceRanges[].label` | string |  |
| `priceRanges[].to` | number |  |
| `priceRanges[].value` | string |  |
| `siteUrl` | string |  |
| `timeZone` | string |  |

## Native endpoint

Through the native Corsizio API, this operation is `GET /account` (base URL `https://api.corsizio.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account-details.md) for the provider-specific parameters and requirements.

