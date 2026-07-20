# Swell: Delete Coupon



```
DELETE https://connect.mindcloud.co/v1/universal/swell/latest/actions/delete-coupon
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Swell `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/swell/latest/actions/delete-coupon?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/swell/latest/actions/delete-coupon?${params}`, {
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
| `id` | string | yes | The Swell coupon ID. |

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

Through the native Swell API, this operation is `DELETE /coupons/:id` (base URL `https://api.swell.store`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-coupon.md) for the provider-specific parameters and requirements.

