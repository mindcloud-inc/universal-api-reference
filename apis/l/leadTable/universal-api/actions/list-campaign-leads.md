# LeadTable: List campaign leads



```
GET https://connect.mindcloud.co/v1/universal/leadTable/latest/actions/list-campaign-leads
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LeadTable `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/leadTable/latest/actions/list-campaign-leads?connectionId=$CONNECTION_ID&limit=25&offset=0&campaignID=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "campaignID": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/leadTable/latest/actions/list-campaign-leads?${params}`, {
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
| `campaignID` | string | yes | The campaign or table whose leads should be listed. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "leads": [
        {}
      ],
      "pages": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `leads` | array<object> | Leads in the campaign. |
| `pages` | object | Pagination details. |

## Native endpoint

Through the native LeadTable API, this operation is `GET /lead/campaign/{campaignID}` (base URL `https://api.lead-table.com/api/v3/external`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-campaign-leads.md) for the provider-specific parameters and requirements.

