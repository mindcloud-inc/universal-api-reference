# Swell: List Coupons



```
GET https://connect.mindcloud.co/v1/universal/swell/latest/actions/list-coupons
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Swell `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/swell/latest/actions/list-coupons?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/swell/latest/actions/list-coupons?${params}`, {
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
      "active": true,
      "codes": {
        "count": 1,
        "limit": 1,
        "page": 1,
        "pageCount": 1,
        "results": [
          {
            "code": "string",
            "dateCreated": "2026-05-07T12:00:00.000Z",
            "id": "string",
            "parentId": "string",
            "useCount": 1,
            "useTotal": 1
          }
        ]
      },
      "currency": "string",
      "dateCreated": "2026-05-07T12:00:00.000Z",
      "discounts": [
        {
          "type": "string",
          "valuePercent": 1,
          "valueType": "string"
        }
      ],
      "id": "string",
      "multiCodes": true,
      "name": "Ava Chen",
      "useCount": 1,
      "useTotal": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `codes.count` | number |  |
| `codes.limit` | number |  |
| `codes.page` | number |  |
| `codes.pageCount` | number |  |
| `codes.results[].code` | string |  |
| `codes.results[].dateCreated` | date |  |
| `codes.results[].id` | string |  |
| `codes.results[].parentId` | string |  |
| `codes.results[].useCount` | number |  |
| `codes.results[].useTotal` | number |  |
| `currency` | string |  |
| `dateCreated` | date |  |
| `discounts[].type` | string |  |
| `discounts[].valuePercent` | number |  |
| `discounts[].valueType` | string |  |
| `id` | string |  |
| `multiCodes` | boolean |  |
| `name` | string |  |
| `useCount` | number |  |
| `useTotal` | number |  |

## Native endpoint

Through the native Swell API, this operation is `GET /coupons` (base URL `https://api.swell.store`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-coupons.md) for the provider-specific parameters and requirements.

