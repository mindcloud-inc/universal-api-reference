# World Health Organization: List Dimension Values

Retrieves values for a dimension from the World Health Organization.

```
GET https://connect.mindcloud.co/v1/universal/worldHealthOrganization/latest/actions/list-dimension-values
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a World Health Organization `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/worldHealthOrganization/latest/actions/list-dimension-values?connectionId=$CONNECTION_ID&limit=25&offset=0&dimensionCode=COUNTRY" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "dimensionCode": "COUNTRY"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/worldHealthOrganization/latest/actions/list-dimension-values?${params}`, {
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
| `dimensionCode` | string | yes | WHO dimension code, such as REGION, COUNTRY, SEX, AGEGROUP, or WORLDBANKINCOMEGROUP. Example: `COUNTRY`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `odataFilter` | string | no | Optional OData $filter expression, for example ParentCode eq 'AMR'. Example: `ParentCode eq 'AMR'`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Code": "string",
      "Dimension": "string",
      "ParentCode": "string",
      "ParentDimension": "string",
      "ParentTitle": "string",
      "Title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Code` | string |  |
| `Dimension` | string |  |
| `ParentCode` | string |  |
| `ParentDimension` | string |  |
| `ParentTitle` | string |  |
| `Title` | string |  |

## Native endpoint

Through the native World Health Organization API, this operation is `GET /DIMENSION/:dimensionCode/DimensionValues` (base URL `https://ghoapi.azureedge.net/api/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-dimension-values.md) for the provider-specific parameters and requirements.

