# lemlist: List Campaign Leads

Retrieves leads from a lemlist campaign.

```
GET https://connect.mindcloud.co/v1/universal/lemlist/latest/actions/list-campaign-leads
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a lemlist `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lemlist/latest/actions/list-campaign-leads?connectionId=$CONNECTION_ID&campaignId=campaign_123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "campaignId": "campaign_123"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lemlist/latest/actions/list-campaign-leads?${params}`, {
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
| `campaignId` | string | yes | The ID of the campaign to retrieve leads from. Example: `campaign_123`. |
| `state` | string | no | Filter leads by their current state. Example: `scanned`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contactId": "string",
      "id": "string",
      "state": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contactId` | string |  |
| `id` | string |  |
| `state` | string |  |

## Native endpoint

Through the native lemlist API, this operation is `GET /campaigns/:campaignId/leads/` (base URL `https://api.lemlist.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-campaign-leads.md) for the provider-specific parameters and requirements.

