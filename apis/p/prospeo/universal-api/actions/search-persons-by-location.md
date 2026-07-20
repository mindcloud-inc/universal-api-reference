# Prospeo: Search Persons by Location

Finds persons in Prospeo by location.

```
GET https://connect.mindcloud.co/v1/universal/prospeo/latest/actions/search-persons-by-location
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Prospeo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/prospeo/latest/actions/search-persons-by-location?connectionId=$CONNECTION_ID&filters=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "filters": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/prospeo/latest/actions/search-persons-by-location?${params}`, {
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
| `filters` | object | yes | Person location search filters. Default: `{"company":{"names":{"include":["Microsoft","Google"]}},"person_location_search":{"include":["United States"]}}`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "company": {},
      "person": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `company` | object |  |
| `person` | object |  |

## Native endpoint

Through the native Prospeo API, this operation is `POST /search-person` (base URL `https://api.prospeo.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-persons-by-location.md) for the provider-specific parameters and requirements.

