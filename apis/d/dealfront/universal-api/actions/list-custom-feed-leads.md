# Dealfront: List Custom Feed Leads

Retrieves leads for a custom feed in Dealfront.

```
GET https://connect.mindcloud.co/v1/universal/dealfront/latest/actions/list-custom-feed-leads
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dealfront `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dealfront/latest/actions/list-custom-feed-leads?connectionId=$CONNECTION_ID&limit=25&offset=0&accountId=1&customFeedId=string&startDate=string&endDate=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "accountId": "1",
  "customFeedId": "string",
  "startDate": "string",
  "endDate": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dealfront/latest/actions/list-custom-feed-leads?${params}`, {
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
| `accountId` | number | yes | ID of the account whose custom feed leads you want to list. |
| `customFeedId` | string | yes | ID of the custom feed whose leads you want to list. |
| `startDate` | string | yes | Start date for the lead search window in YYYY-MM-DD format. |
| `endDate` | string | yes | End date for the lead search window in YYYY-MM-DD format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "firstVisitDate": "2026-05-07T12:00:00.000Z",
        "industries": [
          {
            "name": "Ava Chen"
          }
        ],
        "industry": "string",
        "lastVisitDate": "2026-05-07T12:00:00.000Z",
        "linkedinUrl": "https://example.com",
        "logoUrl": "https://example.com",
        "name": "Ava Chen",
        "quality": 1,
        "status": "string",
        "viewInLeadfeeder": "string",
        "visits": 1,
        "websiteUrl": "https://example.com"
      },
      "id": "string",
      "relationships": {
        "location": {
          "data": {
            "id": "string",
            "type": "string"
          }
        }
      },
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes.firstVisitDate` | date |  |
| `attributes.industries[].name` | string |  |
| `attributes.industry` | string |  |
| `attributes.lastVisitDate` | date |  |
| `attributes.linkedinUrl` | string |  |
| `attributes.logoUrl` | string |  |
| `attributes.name` | string |  |
| `attributes.quality` | number |  |
| `attributes.status` | string |  |
| `attributes.viewInLeadfeeder` | string |  |
| `attributes.visits` | number |  |
| `attributes.websiteUrl` | string |  |
| `id` | string |  |
| `relationships.location.data.id` | string |  |
| `relationships.location.data.type` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Dealfront API, this operation is `GET /accounts/:account_id/custom-feeds/:custom_feed_id/leads` (base URL `https://api.leadfeeder.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-custom-feed-leads.md) for the provider-specific parameters and requirements.

