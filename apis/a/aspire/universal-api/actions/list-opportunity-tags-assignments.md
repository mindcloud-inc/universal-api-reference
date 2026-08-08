# Aspire: List Opportunity Tags Assignments

Retrieves opportunity tags from your Aspire account.

```
GET https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-opportunity-tags-assignments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aspire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-opportunity-tags-assignments?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-opportunity-tags-assignments?${params}`, {
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
| `filter` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "OpportunityID": 1,
      "OpportunityName": "Ava Chen",
      "OpportunityTagID": 1,
      "TagID": 1,
      "TagName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `OpportunityID` | number |  |
| `OpportunityName` | string |  |
| `OpportunityTagID` | number |  |
| `TagID` | number |  |
| `TagName` | string |  |

## Native endpoint

Through the native Aspire API, this operation is `GET OpportunityTags` (base URL `https://{{credentials.environment}}.youraspire.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-opportunity-tags-assignments.md) for the provider-specific parameters and requirements.

