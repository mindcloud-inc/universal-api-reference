# WeSupply: List Updated Item Details

Retrieves updated item details from WeSupply.

```
GET https://connect.mindcloud.co/v1/universal/weSupply/latest/actions/list-updated-item-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WeSupply `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/weSupply/latest/actions/list-updated-item-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/weSupply/latest/actions/list-updated-item-details?${params}`, {
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
| `endDate` | string | no | Inclusive end date for the item update listing window. |
| `itemStatusId` | string | no | Optional item status filter for the listing. |
| `page` | string | no | Page number for paginated item updates. |
| `sort` | string | no | Sort order for the returned item updates. |
| `startDate` | string | no | Inclusive start date for the item update listing window. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Items": "string",
      "LastUpdated": "string",
      "OrderExternalOrderID": "string",
      "OrderID": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Items` | string |  |
| `LastUpdated` | string |  |
| `OrderExternalOrderID` | string |  |
| `OrderID` | string |  |

## Native endpoint

Through the native WeSupply API, this operation is `GET /external/item-update` (base URL `https://{{credentials.subdomain}}.labs.wesupply.xyz/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-updated-item-details.md) for the provider-specific parameters and requirements.

