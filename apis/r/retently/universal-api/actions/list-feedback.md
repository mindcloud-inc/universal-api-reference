# Retently: List Feedback

Retrieves a list of feedback responses from Retently.

```
GET https://connect.mindcloud.co/v1/universal/retently/latest/actions/list-feedback
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Retently `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/retently/latest/actions/list-feedback?connectionId=$CONNECTION_ID&limit=25&offset=0&attributes%5B%5D.name=Ava%20Chen&attributes%5B%5D.op=string&attributes%5B%5D.value=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "attributes[].name": "Ava Chen",
  "attributes[].op": "string",
  "attributes[].value": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/retently/latest/actions/list-feedback?${params}`, {
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
| `email` | string | no | Search responses by a customer's email address; |
| `customerId` | string | no | Search responses by a customer's Retently ID; |
| `campaignId` | string | no | Filter responses by a specific campaign ID; |
| `page` | string | no | The current page number. Default 1; Default: `1`. |
| `limit` | string | no | The items limit. Default 20. Maximum 1,000; Default: `20`. |
| `sort` | string | no | The sort option. Use '-' for DESC. Default '-createdDate'; |
| `startDate` | string | no | ISO format or UNIX timestamp; |
| `endDate` | string | no | ISO format or UNIX timestamp; |
| `attributes[]` | array<string> | no | Filter by customer properties. See Attributes Filtering section below; |
| `match` | string | no | Logic for multiple attribute filters. Values: 'all' (AND, default), 'any' (OR); Default: `all`. |
| `attributes[].name` | string | yes | Attribute field name |
| `attributes[].op` | string | yes | Filter operator |
| `attributes[].value` | string | yes | Attribute match value |

## Response

```json
{
  "success": true,
  "data": [
    {
      "comment": "string",
      "companyName": "Ava Chen",
      "createdDate": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "feedbackTags": [
        "string"
      ],
      "firstName": "Ava",
      "lastName": "Chen",
      "score": 1,
      "tags": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `comment` | string |  |
| `companyName` | string |  |
| `createdDate` | date |  |
| `email` | string |  |
| `feedbackTags` | array<string> |  |
| `firstName` | string |  |
| `lastName` | string |  |
| `score` | number |  |
| `tags` | array<string> |  |

## Native endpoint

Through the native Retently API, this operation is `GET /api/v2/feedback` (base URL `https://app.retently.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-feedback.md) for the provider-specific parameters and requirements.

