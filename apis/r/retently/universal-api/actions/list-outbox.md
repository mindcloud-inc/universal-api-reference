# Retently: List Outbox

Retrieves a list of sent surveys from Retently.

```
GET https://connect.mindcloud.co/v1/universal/retently/latest/actions/list-outbox
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Retently `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/retently/latest/actions/list-outbox?connectionId=$CONNECTION_ID&limit=25&offset=0&attributes%5B%5D.name=Ava%20Chen&attributes%5B%5D.op=string&attributes%5B%5D.value=string" \
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

const response = await fetch(`https://connect.mindcloud.co/v1/universal/retently/latest/actions/list-outbox?${params}`, {
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
| `email` | string | no | Find a customer's outbox records by email address; |
| `page` | string | no | The current page number. Default 1; Default: `1`. |
| `limit` | string | no | The items limit. Default 20. Maximum 1,000; Default: `20`. |
| `sort` | string | no | The sort option. Use '-surveyCreatedDate' for results in descending order; Default '-surveyCreatedDate'; |
| `campaignId` | string | no | Filter by campaign ID; |
| `startDate` | string | no | Filter surveys sent after this date. ISO format or UNIX timestamp; |
| `endDate` | string | no | Filter surveys sent before this date. ISO format or UNIX timestamp; |
| `channel` | string | no | Filter by survey channel. Values: email, link, inapp, intercom; |
| `sentBy` | string | no | Filter by how the survey was sent. Values: campaign, reminder, manual, test, imported; |
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
      "additionalRecipients": [
        "string"
      ],
      "attributes": {},
      "campaign": "string",
      "campaignId": "string",
      "channel": "string",
      "companyId": "string",
      "companyName": "Ava Chen",
      "customerId": "string",
      "detailedStatus": {},
      "email": "ava@example.com",
      "firstName": "Ava",
      "lastName": "Chen",
      "mandrillMessageId": "string",
      "personTags": [
        "string"
      ],
      "responseId": "string",
      "sentBy": "string",
      "sentDate": "string",
      "status": "string",
      "subject": "string",
      "surveyId": "string",
      "surveyTemplateId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `additionalRecipients` | array<string> |  |
| `attributes` | object |  |
| `campaign` | string |  |
| `campaignId` | string |  |
| `channel` | string |  |
| `companyId` | string |  |
| `companyName` | string |  |
| `customerId` | string |  |
| `detailedStatus` | object |  |
| `email` | string |  |
| `firstName` | string |  |
| `lastName` | string |  |
| `mandrillMessageId` | string |  |
| `personTags` | array<string> |  |
| `responseId` | string |  |
| `sentBy` | string |  |
| `sentDate` | string |  |
| `status` | string |  |
| `subject` | string |  |
| `surveyId` | string |  |
| `surveyTemplateId` | string |  |

## Native endpoint

Through the native Retently API, this operation is `GET /api/v2/outbox` (base URL `https://app.retently.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-outbox.md) for the provider-specific parameters and requirements.

