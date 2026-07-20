# Smoove: List Campaign Recipients

Retrieves recipient responses for a Smoove email campaign.

```
GET https://connect.mindcloud.co/v1/universal/smoove/latest/actions/list-campaign-recipients
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Smoove `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smoove/latest/actions/list-campaign-recipients?connectionId=$CONNECTION_ID&limit=25&offset=0&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smoove/latest/actions/list-campaign-recipients?${params}`, {
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
| `id` | string | yes |  |
| `by` | list | no | One of: `CampaignId`, `ExternalId`. Default: `CampaignId`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": 1,
      "lastName": "Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string |  |
| `firstName` | string |  |
| `id` | number |  |
| `lastName` | string |  |

## Native endpoint

Through the native Smoove API, this operation is `GET /v1/Campaigns/:id/Recipients` (base URL `https://rest.smoove.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-campaign-recipients.md) for the provider-specific parameters and requirements.

