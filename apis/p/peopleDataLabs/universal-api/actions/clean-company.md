# People Data Labs: Clean Company



```
GET https://connect.mindcloud.co/v1/universal/peopleDataLabs/latest/actions/clean-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a People Data Labs `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/peopleDataLabs/latest/actions/clean-company?connectionId=$CONNECTION_ID&profile=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "profile": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/peopleDataLabs/latest/actions/clean-company?${params}`, {
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
| `profile` | string | yes | Company profile URL to standardize into canonical company data. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "facebookUrl": "https://example.com",
      "founded": 1,
      "fuzzyMatch": true,
      "id": "string",
      "industry": "string",
      "industryV2": "string",
      "linkedinId": "https://example.com",
      "linkedinUrl": "https://example.com",
      "location": {
        "addressLine2": "string",
        "continent": "string",
        "country": "string",
        "geo": "string",
        "locality": "string",
        "metro": "string",
        "name": "Ava Chen",
        "postalCode": "string",
        "region": "string",
        "streetAddress": "string"
      },
      "name": "Ava Chen",
      "score": 1,
      "size": "string",
      "status": 1,
      "twitterUrl": "https://example.com",
      "type": "string",
      "website": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `facebookUrl` | string |  |
| `founded` | number |  |
| `fuzzyMatch` | boolean |  |
| `id` | string |  |
| `industry` | string |  |
| `industryV2` | string |  |
| `linkedinId` | string |  |
| `linkedinUrl` | string |  |
| `location.addressLine2` | string |  |
| `location.continent` | string |  |
| `location.country` | string |  |
| `location.geo` | string |  |
| `location.locality` | string |  |
| `location.metro` | string |  |
| `location.name` | string |  |
| `location.postalCode` | string |  |
| `location.region` | string |  |
| `location.streetAddress` | string |  |
| `name` | string |  |
| `score` | number |  |
| `size` | string |  |
| `status` | number |  |
| `twitterUrl` | string |  |
| `type` | string |  |
| `website` | string |  |

## Native endpoint

Through the native People Data Labs API, this operation is `GET /company/clean` (base URL `https://api.peopledatalabs.com/v5`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/clean-company.md) for the provider-specific parameters and requirements.

