# Avalara AvaTax: List Parameters



```
GET https://connect.mindcloud.co/v1/universal/avalara/latest/actions/list-parameters
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Avalara AvaTax `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/avalara/latest/actions/list-parameters?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/avalara/latest/actions/list-parameters?${params}`, {
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
      "attributeType": "string",
      "category": "string",
      "dataType": "string",
      "helpText": "string",
      "id": 1,
      "isNeededForCalculation": true,
      "isNeededForClassification": true,
      "isNeededForReturns": true,
      "label": "string",
      "measurementType": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributeType` | string |  |
| `category` | string |  |
| `dataType` | string |  |
| `helpText` | string |  |
| `id` | number |  |
| `isNeededForCalculation` | boolean |  |
| `isNeededForClassification` | boolean |  |
| `isNeededForReturns` | boolean |  |
| `label` | string |  |
| `measurementType` | string |  |
| `name` | string |  |

## Native endpoint

Through the native Avalara AvaTax API, this operation is `GET definitions/parameters` (base URL `{{credentials.environment}}`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-parameters.md) for the provider-specific parameters and requirements.

