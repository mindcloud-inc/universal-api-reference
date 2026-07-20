# LaGrowthMachine: Get Campaign

Retrieves a campaign from LaGrowthMachine.

```
GET https://connect.mindcloud.co/v1/universal/laGrowthMachine/latest/actions/get-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LaGrowthMachine `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/laGrowthMachine/latest/actions/get-campaign?connectionId=$CONNECTION_ID&campaignId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "campaignId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/laGrowthMachine/latest/actions/get-campaign?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "activated": 1,
      "audienceName": "Ava Chen",
      "audienceSize": 1,
      "converted": 1,
      "createdAt": 1,
      "description": "string",
      "id": "string",
      "identityFirstname": "Ava",
      "identityId": "string",
      "identityLastname": "Chen",
      "language": "string",
      "launchedAt": 1,
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
| `activated` | number | Activated lead count. |
| `audienceName` | string | Audience name linked to the campaign. |
| `audienceSize` | number | Audience size. |
| `converted` | number | Converted lead count. |
| `createdAt` | number | Campaign creation timestamp. |
| `description` | string | Campaign description. |
| `id` | string | Campaign identifier. |
| `identityFirstname` | string | Identity first name. |
| `identityId` | string | Linked identity ID. |
| `identityLastname` | string | Identity last name. |
| `language` | string | Campaign language. |
| `launchedAt` | number | Campaign launch timestamp. |
| `modifiedAt` | number | Campaign last update timestamp. |
| `name` | string | Campaign name. |
| `status` | string | Campaign status. |

## Native endpoint

Through the native LaGrowthMachine API, this operation is `GET /campaigns/:campaignId` (base URL `https://apiv2.lagrowthmachine.com/flow`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-campaign.md) for the provider-specific parameters and requirements.

