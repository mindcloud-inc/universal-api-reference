# Walmart: Get Item Count by Groups

Retrieve the total number of items based on variant group information.

```
GET https://connect.mindcloud.co/v1/universal/walmart/latest/actions/get-item-count-by-groups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Walmart `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/walmart/latest/actions/get-item-count-by-groups?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/walmart/latest/actions/get-item-count-by-groups?${params}`, {
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
| `variantGroupId` | string | no | Retrieve all items with the same variant id |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "variantGroupId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `variantGroupId` | string |  |

## Native endpoint

Through the native Walmart API, this operation is `GET /v3/items/groups/count` (base URL `https://{{credentials.environment}}.walmartapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-item-count-by-groups.md) for the provider-specific parameters and requirements.

