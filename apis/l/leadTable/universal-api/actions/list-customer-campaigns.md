# LeadTable: List customer campaigns



```
GET https://connect.mindcloud.co/v1/universal/leadTable/latest/actions/list-customer-campaigns
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LeadTable `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/leadTable/latest/actions/list-customer-campaigns?connectionId=$CONNECTION_ID&limit=25&offset=0&customerID=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "customerID": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/leadTable/latest/actions/list-customer-campaigns?${params}`, {
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
| `customerID` | string | yes | The customer whose campaigns should be listed. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "campaigns": [
        {}
      ],
      "pagination": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campaigns` | array<object> | Campaigns for the selected customer. |
| `pagination` | object | Pagination details. |

## Native endpoint

Through the native LeadTable API, this operation is `GET /campaign/all/{customerID}` (base URL `https://api.lead-table.com/api/v3/external`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-customer-campaigns.md) for the provider-specific parameters and requirements.

