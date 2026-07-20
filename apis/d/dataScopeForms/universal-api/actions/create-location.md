# DataScope Forms: Create Location

Creates a new location in DataScope Forms.

```
POST https://connect.mindcloud.co/v1/universal/dataScopeForms/latest/actions/create-location
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DataScope Forms `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dataScopeForms/latest/actions/create-location" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dataScopeForms/latest/actions/create-location', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `location.address` | string | no | Address of the location. |
| `location.city` | string | no | City of the location. |
| `location.code` | string | no | Code of the location. |
| `location.company_code` | string | no | Code of the company for the location. |
| `location.company_name` | string | no | Company name for the location. |
| `location.country` | string | no | Country of the location. |
| `location.description` | string | no | Description of the location. |
| `location.email` | string | no | Email of the location. |
| `location.latitude` | number | no | Latitude of the location. |
| `location.longitude` | number | no | Longitude of the location. |
| `location.name` | string | no | Name of the location. |
| `location.phone` | string | no | Phone number of the location. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": "string",
      "city": "string",
      "code": "string",
      "company_code": "string",
      "company_name": "Ava Chen",
      "country": "string",
      "description": "string",
      "email": "ava@example.com",
      "id": 1,
      "latitude": 1,
      "longitude": 1,
      "name": "Ava Chen",
      "phone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string |  |
| `city` | string |  |
| `code` | string |  |
| `company_code` | string |  |
| `company_name` | string |  |
| `country` | string |  |
| `description` | string |  |
| `email` | string |  |
| `id` | number |  |
| `latitude` | number |  |
| `longitude` | number |  |
| `name` | string |  |
| `phone` | string |  |

## Native endpoint

Through the native DataScope Forms API, this operation is `POST /external/locations` (base URL `https://www.mydatascope.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-location.md) for the provider-specific parameters and requirements.

