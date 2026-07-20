# NCEI Climate Data: Get Location Category

Retrieves location category details from NCEI Climate Data.

```
GET https://connect.mindcloud.co/v1/universal/nCEIClimateData/latest/actions/get-location-category
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NCEI Climate Data `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nCEIClimateData/latest/actions/get-location-category?connectionId=$CONNECTION_ID&locationCategoryId=ST" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "locationCategoryId": "ST"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nCEIClimateData/latest/actions/get-location-category?${params}`, {
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
| `locationCategoryId` | string | yes | Location category identifier to retrieve, for example ST or CITY. Example: `ST`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `name` | string |  |

## Native endpoint

Through the native NCEI Climate Data API, this operation is `GET /locationcategories/[:locationCategoryId]` (base URL `https://www.ncei.noaa.gov/cdo-web/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-location-category.md) for the provider-specific parameters and requirements.

