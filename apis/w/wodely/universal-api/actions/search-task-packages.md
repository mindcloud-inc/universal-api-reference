# Wodely: Search Task Packages



```
GET https://connect.mindcloud.co/v1/universal/wodely/latest/actions/search-task-packages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wodely `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wodely/latest/actions/search-task-packages?connectionId=$CONNECTION_ID&taskGuid=your-task-guid" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "taskGuid": "your-task-guid"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wodely/latest/actions/search-task-packages?${params}`, {
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
| `taskGuid` | string | yes | Task identifier returned by Wodely. Example: `your-task-guid`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "field1": "string",
      "field2": "string",
      "field3": "string",
      "field4": "string",
      "field5": "string",
      "id": 1,
      "labelId": "string",
      "orderId": "string",
      "packageTypeDesc": "string",
      "packageTypeId": 1,
      "price": 1,
      "productDesc": "string",
      "productId": "string",
      "quantity": 1,
      "taskId": 1,
      "weight": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `field1` | string | Custom field 1. |
| `field2` | string | Custom field 2. |
| `field3` | string | Custom field 3. |
| `field4` | string | Custom field 4. |
| `field5` | string | Custom field 5. |
| `id` | number | Package identifier. |
| `labelId` | string | Package label or barcode identifier. |
| `orderId` | string | Order identifier associated with the package. |
| `packageTypeDesc` | string | Package type description. |
| `packageTypeId` | number | Package type identifier. |
| `price` | number | Package price or line total. |
| `productDesc` | string | Package product description. |
| `productId` | string | Product or item identifier. |
| `quantity` | number | Package quantity. |
| `taskId` | number | Numeric task identifier linked to the package. |
| `weight` | number | Package weight. |

## Native endpoint

Through the native Wodely API, this operation is `POST /v2/taskPackages/search` (base URL `https://api.wodely.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-task-packages.md) for the provider-specific parameters and requirements.

