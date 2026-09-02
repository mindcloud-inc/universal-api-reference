# Jetbuilt: Get Project Purchasing



```
GET https://connect.mindcloud.co/v1/universal/jetbuilt/latest/actions/get-project-purchasing
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jetbuilt `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jetbuilt/latest/actions/get-project-purchasing?connectionId=$CONNECTION_ID&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jetbuilt/latest/actions/get-project-purchasing?${params}`, {
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
| `projectId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "lineItems": [
        {
          "cost": "string",
          "fullName": "Ava Chen",
          "ids": [
            1
          ],
          "orderNotes": {},
          "orderQuantity": "string",
          "orderStatus": "string",
          "projectQuantity": "string",
          "shortDescription": "string",
          "soldChangeOrder": true,
          "source": {},
          "totalOrderCost": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `lineItems[].cost` | string |  |
| `lineItems[].fullName` | string |  |
| `lineItems[].ids[]` | number |  |
| `lineItems[].orderNotes` | object |  |
| `lineItems[].orderQuantity` | string |  |
| `lineItems[].orderStatus` | string |  |
| `lineItems[].projectQuantity` | string |  |
| `lineItems[].shortDescription` | string |  |
| `lineItems[].soldChangeOrder` | boolean |  |
| `lineItems[].source` | object |  |
| `lineItems[].totalOrderCost` | string |  |

## Native endpoint

Through the native Jetbuilt API, this operation is `GET projects/[:projectId]/purchasing` (base URL `https://app.jetbuilt.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project-purchasing.md) for the provider-specific parameters and requirements.

