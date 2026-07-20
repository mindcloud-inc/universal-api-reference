# Chatvolt AI: List Contacts

Retrieves contacts from Chatvolt AI.

```
GET https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/contacts-get
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatvolt AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/contacts-get?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/contacts-get?${params}`, {
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
| `offset` | number | no | Number of records to skip for pagination. |
| `limit` | number | no | Maximum number of records to return. |
| `search` | string | no | Search term for email, phone number, first name, or last name. |
| `tags[]` | array<string> | no | List of tags to filter by. |
| `crmScenario` | string | no | Filter by CRM Scenario ID. |
| `crmStep` | string | no | Filter by CRM Step ID. |
| `conversationStatus` | string | no | Filter by conversation status. |
| `agent` | string | no | Filter by Agent ID. |
| `priority` | string | no | Filter by conversation priority. |
| `startDate` | string | no | Filter contacts created on or after this date. |
| `endDate` | string | no | Filter contacts created on or before this date. |
| `hasEmail` | boolean | no | Filter contacts that have an email address. |
| `hasPhone` | boolean | no | Filter contacts that have a phone number. |
| `channel` | string | no | Filter by conversation channel. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contacts": [
        "string"
      ],
      "count": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contacts` | array | Contacts. |
| `count` | number | Count. |

## Native endpoint

Through the native Chatvolt AI API, this operation is `GET /contacts` (base URL `https://api.chatvolt.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/contacts-get.md) for the provider-specific parameters and requirements.

