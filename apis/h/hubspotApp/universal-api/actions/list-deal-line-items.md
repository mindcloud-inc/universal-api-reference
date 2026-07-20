# HubSpot: List Deal Line Items

Retrieves line items associated with a HubSpot deal.

```
GET https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/list-deal-line-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HubSpot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/list-deal-line-items?connectionId=$CONNECTION_ID&dealId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "dealId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/list-deal-line-items?${params}`, {
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
| `dealId` | string | yes | The unique ID of the deal whose line item associations to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | The associated line item record ID. |
| `type` | string | The HubSpot association type identifier. |

## Native endpoint

Through the native HubSpot API, this operation is `GET crm/v3/objects/deals/:dealId/associations/line_items` (base URL `https://api.hubapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-deal-line-items.md) for the provider-specific parameters and requirements.

