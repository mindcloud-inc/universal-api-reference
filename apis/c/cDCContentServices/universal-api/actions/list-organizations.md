# CDC Content Services: List Organizations

Retrieves organizations from CDC Content Services.

```
GET https://connect.mindcloud.co/v1/universal/cDCContentServices/latest/actions/list-organizations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CDC Content Services `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cDCContentServices/latest/actions/list-organizations?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cDCContentServices/latest/actions/list-organizations?${params}`, {
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
      "city": "string",
      "country": "string",
      "county": "string",
      "default": true,
      "description": "string",
      "geoNameId": 1,
      "id": 1,
      "members": [
        {}
      ],
      "name": "Ava Chen",
      "stateProvince": "string",
      "type": "string",
      "website": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `city` | string | City. |
| `country` | string | Country code. |
| `county` | string | County. |
| `default` | boolean | Whether this is a default organization entry. |
| `description` | string | Organization description. |
| `geoNameId` | number | GeoName identifier. |
| `id` | number | Organization identifier. |
| `members` | array<object> | Organization member entries. |
| `name` | string | Organization name. |
| `stateProvince` | string | State or province. |
| `type` | string | Organization type. |
| `website` | array<object> | Organization website entries. |

## Native endpoint

Through the native CDC Content Services API, this operation is `GET /v2/resources/organizations` (base URL `https://tools.cdc.gov/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-organizations.md) for the provider-specific parameters and requirements.

