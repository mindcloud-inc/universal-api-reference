# LaGrowthMachine: Get Campaign Lead Stats

Retrieves campaign lead stats from LaGrowthMachine.

```
GET https://connect.mindcloud.co/v1/universal/laGrowthMachine/latest/actions/get-campaign-lead-stats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LaGrowthMachine `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/laGrowthMachine/latest/actions/get-campaign-lead-stats?connectionId=$CONNECTION_ID&campaignId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "campaignId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/laGrowthMachine/latest/actions/get-campaign-lead-stats?${params}`, {
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
| `campaignId` | string | yes | Campaign ID. |
| `getLeadsAfter` | string | no | Lead ID cursor for the next page. |
| `getLeadsBefore` | string | no | Lead ID cursor for the previous page. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "action_todo": "string",
      "companyName": "Ava Chen",
      "companyUrl": "https://example.com",
      "count": 1,
      "email": "ava@example.com",
      "firstname": "Ava",
      "hasLess": true,
      "hasMore": true,
      "id": "string",
      "lastname": "Chen",
      "linkedinUrl": "https://example.com",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `action_todo` | string | Next action marker for the lead. |
| `companyName` | string | Company name. |
| `companyUrl` | string | Company URL. |
| `count` | number | Total matching leads. |
| `email` | string | Lead email. |
| `firstname` | string | Lead first name. |
| `hasLess` | boolean | Whether a previous page exists. |
| `hasMore` | boolean | Whether a next page exists. |
| `id` | string | Lead identifier. |
| `lastname` | string | Lead last name. |
| `linkedinUrl` | string | Lead LinkedIn profile URL. |
| `status` | string | Lead campaign status. |

## Native endpoint

Through the native LaGrowthMachine API, this operation is `GET /campaigns/:campaignId/statsleads` (base URL `https://apiv2.lagrowthmachine.com/flow`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-campaign-lead-stats.md) for the provider-specific parameters and requirements.

