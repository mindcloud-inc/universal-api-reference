# World Health Organization: List Indicator Dimensions

Retrieves indicator dimensions from the World Health Organization.

```
GET https://connect.mindcloud.co/v1/universal/worldHealthOrganization/latest/actions/list-indicator-dimensions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a World Health Organization `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/worldHealthOrganization/latest/actions/list-indicator-dimensions?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/worldHealthOrganization/latest/actions/list-indicator-dimensions?${params}`, {
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
| `odataFilter` | string | no | Optional OData $filter expression, for example IndicatorCode eq 'WHOSIS_000001'. Example: `IndicatorCode eq 'WHOSIS_000001'`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Dimension": "string",
      "DimensionName": "Ava Chen",
      "IndicatorCode": "string",
      "Language": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Dimension` | string |  |
| `DimensionName` | string |  |
| `IndicatorCode` | string |  |
| `Language` | string |  |

## Native endpoint

Through the native World Health Organization API, this operation is `GET /IndicatorDimension` (base URL `https://ghoapi.azureedge.net/api/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-indicator-dimensions.md) for the provider-specific parameters and requirements.

