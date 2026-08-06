# Avalara AvaTax: List Jurisdictions Hierarchy



```
GET https://connect.mindcloud.co/v1/universal/avalara/latest/actions/list-jurisdictions-hierarchy
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Avalara AvaTax `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/avalara/latest/actions/list-jurisdictions-hierarchy?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/avalara/latest/actions/list-jurisdictions-hierarchy?${params}`, {
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
      "code": "string",
      "country": "string",
      "county": "string",
      "countyFips": "string",
      "createDate": "2026-05-07T12:00:00.000Z",
      "effectiveDate": "2026-05-07T12:00:00.000Z",
      "endDate": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "isAcm": true,
      "isLocalAdmin": true,
      "isSst": true,
      "modifiedDate": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "placeFips": "string",
      "region": "string",
      "shortName": "Ava Chen",
      "stateFips": "string",
      "taxAuthorityTypeId": 1,
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `city` | string |  |
| `code` | string |  |
| `country` | string |  |
| `county` | string |  |
| `countyFips` | string |  |
| `createDate` | date |  |
| `effectiveDate` | date |  |
| `endDate` | date |  |
| `id` | number |  |
| `isAcm` | boolean |  |
| `isLocalAdmin` | boolean |  |
| `isSst` | boolean |  |
| `modifiedDate` | date |  |
| `name` | string |  |
| `placeFips` | string |  |
| `region` | string |  |
| `shortName` | string |  |
| `stateFips` | string |  |
| `taxAuthorityTypeId` | number |  |
| `type` | string |  |

## Native endpoint

Through the native Avalara AvaTax API, this operation is `GET definitions/jurisdictions` (base URL `{{credentials.environment}}`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-jurisdictions-hierarchy.md) for the provider-specific parameters and requirements.

