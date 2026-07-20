# DataScope Forms: List Locations

Retrieves locations from DataScope Forms.

```
GET https://connect.mindcloud.co/v1/universal/dataScopeForms/latest/actions/list-locations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DataScope Forms `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dataScopeForms/latest/actions/list-locations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dataScopeForms/latest/actions/list-locations?${params}`, {
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
      "address": "string",
      "city": "string",
      "code": "string",
      "company_code": "string",
      "company_name": "Ava Chen",
      "country": "string",
      "description": "string",
      "id": 1,
      "latitude": 1,
      "longitude": 1,
      "name": "Ava Chen",
      "phone": "string",
      "region": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string | Address of the location. |
| `city` | string | City of the location. |
| `code` | string | Code of the location. |
| `company_code` | string | Code of the company. |
| `company_name` | string | Name of the company. |
| `country` | string | Country of the location. |
| `description` | string | Description of the location. |
| `id` | number | Internal identifier of the location. |
| `latitude` | number | Latitude GPS coordinate. |
| `longitude` | number | Longitude GPS coordinate. |
| `name` | string | Name of the location. |
| `phone` | string | Phone number of the location. |
| `region` | string | Region of the location. |

## Native endpoint

Through the native DataScope Forms API, this operation is `GET /external/locations` (base URL `https://www.mydatascope.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-locations.md) for the provider-specific parameters and requirements.

