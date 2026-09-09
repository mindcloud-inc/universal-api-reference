# Walmart: Get Taxonomy

Retrieve items taxonomy information.

```
GET https://connect.mindcloud.co/v1/universal/walmart/latest/actions/get-taxonomy
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Walmart `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/walmart/latest/actions/get-taxonomy?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/walmart/latest/actions/get-taxonomy?${params}`, {
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
| `feedType` | list<string> | no | The type of feed defines the nature of the request. Select an option from the drop-down list based on the type of taxonomy details you need to retrieve. Examples: - `MP_WFS_ITEM` - indicates WFS Item - `MP_ITEM` - Indicates Seller Fulfilled Item Example: `MP_ITEM`. |
| `version` | list<list> | no | The status of an item in the overall lifecycle. Example: `5.0`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "category": "string",
      "description": "string",
      "productTypeGroup": [
        {
          "department": [
            {
              "departmentName": "Ava Chen",
              "departmentNumber": "string"
            }
          ],
          "description": "string",
          "productType": [
            {
              "description": "string",
              "productTypeName": "Ava Chen"
            }
          ],
          "productTypeGroupName": "Ava Chen"
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
| `category` | string |  |
| `description` | string |  |
| `productTypeGroup[].department[].departmentName` | string |  |
| `productTypeGroup[].department[].departmentNumber` | string |  |
| `productTypeGroup[].description` | string |  |
| `productTypeGroup[].productType[].description` | string |  |
| `productTypeGroup[].productType[].productTypeName` | string |  |
| `productTypeGroup[].productTypeGroupName` | string |  |

## Native endpoint

Through the native Walmart API, this operation is `GET /v3/items/taxonomy` (base URL `https://{{credentials.environment}}.walmartapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-taxonomy.md) for the provider-specific parameters and requirements.

