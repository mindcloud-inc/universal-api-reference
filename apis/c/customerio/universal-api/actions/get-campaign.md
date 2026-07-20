# Customer.io: Get Campaign

Retrieves a campaign from Customer.io.

```
GET https://connect.mindcloud.co/v1/universal/customerio/latest/actions/get-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Customer.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/customerio/latest/actions/get-campaign?connectionId=$CONNECTION_ID&campaignId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "campaignId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/customerio/latest/actions/get-campaign?${params}`, {
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
| `campaignId` | number | yes | The numeric ID of the campaign you want to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "actions": [
        {}
      ],
      "active": true,
      "created": 1,
      "deduplicateId": "string",
      "firstStarted": 1,
      "id": 1,
      "name": "Ava Chen",
      "state": "string",
      "tags": [
        "string"
      ],
      "type": "string",
      "updated": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actions` | array<object> | The actions configured in the campaign. |
| `active` | boolean | Whether the campaign is active. |
| `created` | number | Unix timestamp when the campaign was created. |
| `deduplicateId` | string | The deduplication token for the campaign. |
| `firstStarted` | number | Unix timestamp when the campaign first started. |
| `id` | number | The identifier for the campaign. |
| `name` | string | The name of the campaign. |
| `state` | string | The campaign state. |
| `tags` | array<string> | Tags applied to the campaign. |
| `type` | string | The campaign trigger type. |
| `updated` | number | Unix timestamp when the campaign was last updated. |

## Native endpoint

Through the native Customer.io API, this operation is `GET /v1/campaigns/:campaign_id` (base URL `https://api.customer.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-campaign.md) for the provider-specific parameters and requirements.

