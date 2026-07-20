# Dealfront: List Visits

Retrieves visits from Dealfront.

```
GET https://connect.mindcloud.co/v1/universal/dealfront/latest/actions/list-visits
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dealfront `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dealfront/latest/actions/list-visits?connectionId=$CONNECTION_ID&limit=25&offset=0&accountId=1&startDate=string&endDate=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "accountId": "1",
  "startDate": "string",
  "endDate": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dealfront/latest/actions/list-visits?${params}`, {
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
| `accountId` | number | yes | ID of the account whose visits you want to list. |
| `startDate` | string | yes | Start date for the visit search window in YYYY-MM-DD format. |
| `endDate` | string | yes | End date for the visit search window in YYYY-MM-DD format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "countryCode": "string",
        "date": "2026-05-07T12:00:00.000Z",
        "deviceType": "string",
        "hour": 1,
        "keyword": "string",
        "landingPagePath": "string",
        "leadId": "string",
        "medium": "string",
        "pageDepth": 1,
        "queryTerm": "string",
        "referringUrl": "https://example.com",
        "source": "string",
        "startedAt": "string",
        "visitLength": 1,
        "visitorEmail": "ava@example.com",
        "visitRoute": [
          {
            "pageTitle": "string",
            "pageUrl": "https://example.com"
          }
        ]
      },
      "id": "string",
      "relationships": {
        "location": {
          "data": {
            "id": "string"
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
| `attributes.countryCode` | string |  |
| `attributes.date` | date |  |
| `attributes.deviceType` | string |  |
| `attributes.hour` | number |  |
| `attributes.keyword` | string |  |
| `attributes.landingPagePath` | string |  |
| `attributes.leadId` | string |  |
| `attributes.medium` | string |  |
| `attributes.pageDepth` | number |  |
| `attributes.queryTerm` | string |  |
| `attributes.referringUrl` | string |  |
| `attributes.source` | string |  |
| `attributes.startedAt` | string |  |
| `attributes.visitLength` | number |  |
| `attributes.visitorEmail` | string |  |
| `attributes.visitRoute[].pageTitle` | string |  |
| `attributes.visitRoute[].pageUrl` | string |  |
| `id` | string |  |
| `relationships.location.data.id` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Dealfront API, this operation is `GET /accounts/:account_id/visits` (base URL `https://api.leadfeeder.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-visits.md) for the provider-specific parameters and requirements.

