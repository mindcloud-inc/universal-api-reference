# Rithum for Brands: List Profiles



```
GET https://connect.mindcloud.co/v1/universal/rithumForBrands/latest/actions/list-profiles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rithum for Brands `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rithumForBrands/latest/actions/list-profiles?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rithumForBrands/latest/actions/list-profiles?${params}`, {
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
      "accountName": "Ava Chen",
      "companyName": "Ava Chen",
      "currencyCode": "string",
      "defaultDistributionCenterID": 1,
      "id": 1,
      "timeZoneDescription": "string",
      "timeZoneRegion": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountName` | string |  |
| `companyName` | string |  |
| `currencyCode` | string |  |
| `defaultDistributionCenterID` | number |  |
| `id` | number |  |
| `timeZoneDescription` | string |  |
| `timeZoneRegion` | string |  |

## Native endpoint

Through the native Rithum for Brands API, this operation is `GET Profiles` (base URL `https://api.channeladvisor.com/v1/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-profiles.md) for the provider-specific parameters and requirements.

