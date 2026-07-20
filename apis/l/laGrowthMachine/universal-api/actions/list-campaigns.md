# LaGrowthMachine: List Campaigns

Retrieves campaigns from LaGrowthMachine.

```
GET https://connect.mindcloud.co/v1/universal/laGrowthMachine/latest/actions/list-campaigns
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LaGrowthMachine `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/laGrowthMachine/latest/actions/list-campaigns?connectionId=$CONNECTION_ID&limit=25&skip=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "limit": "25",
  "skip": "0"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/laGrowthMachine/latest/actions/list-campaigns?${params}`, {
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
| `limit` | number | yes | Maximum number of campaigns to return. Default: `25`. |
| `skip` | number | yes | Number of records to skip for pagination. Default: `0`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": 1,
      "description": "string",
      "id": "string",
      "language": "string",
      "launchedAt": 1,
      "leadsCount": 1,
      "modifiedAt": 1,
      "name": "Ava Chen",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | number | Campaign creation timestamp. |
| `description` | string | Campaign description. |
| `id` | string | Campaign identifier. |
| `language` | string | Campaign language. |
| `launchedAt` | number | Campaign launch timestamp. |
| `leadsCount` | number | Number of leads in the campaign. |
| `modifiedAt` | number | Campaign last update timestamp. |
| `name` | string | Campaign name. |
| `status` | string | Campaign status. |

## Native endpoint

Through the native LaGrowthMachine API, this operation is `GET /campaigns` (base URL `https://apiv2.lagrowthmachine.com/flow`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-campaigns.md) for the provider-specific parameters and requirements.

