# World Health Organization: List Region Countries

Retrieves region-country mappings from the World Health Organization.

```
GET https://connect.mindcloud.co/v1/universal/worldHealthOrganization/latest/actions/list-region-countries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a World Health Organization `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/worldHealthOrganization/latest/actions/list-region-countries?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/worldHealthOrganization/latest/actions/list-region-countries?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `odataFilter` | string | no | Optional OData $filter expression, for example RegionCode eq 'AMR' or CountryCode eq 'BRA'. Example: `CountryCode eq 'BRA'`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "CountryCode": "string",
      "CountryName": "Ava Chen",
      "Language": "string",
      "RegionCode": "string",
      "RegionName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `CountryCode` | string |  |
| `CountryName` | string |  |
| `Language` | string |  |
| `RegionCode` | string |  |
| `RegionName` | string |  |

## Native endpoint

Through the native World Health Organization API, this operation is `GET /RegionCountry` (base URL `https://ghoapi.azureedge.net/api/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-region-countries.md) for the provider-specific parameters and requirements.

