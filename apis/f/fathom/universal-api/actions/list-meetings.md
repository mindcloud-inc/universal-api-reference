# Fathom: List Meetings

Retrieves meetings from Fathom.

```
GET https://connect.mindcloud.co/v1/universal/fathom/latest/actions/list-meetings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fathom `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fathom/latest/actions/list-meetings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fathom/latest/actions/list-meetings?${params}`, {
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
| `cursor` | string | no | Cursor for pagination. |
| `createdAfter` | date | no | Filter meetings created after this timestamp (ISO 8601). |
| `createdBefore` | date | no | Filter meetings created before this timestamp (ISO 8601). |
| `teams` | string | no | Filter by one or more team names. Accepts multiple values as an array. |
| `recordedBy` | string | no | Filter by one or more recorder email addresses. Accepts multiple values as an array. |
| `calendarInviteesDomains` | string | no | Filter by invitee domains. Pass one value per domain. Accepts multiple values as an array. |
| `calendarInviteesDomainsType` | string | no | all, only_internal, or one_or_more_external. |
| `includeActionItems` | boolean | no | Include action items for each meeting. |
| `includeCrmMatches` | boolean | no | Include CRM matches for each meeting. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "items": [
        {}
      ],
      "limit": 1,
      "nextCursor": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `items` | array<object> |  |
| `limit` | number |  |
| `nextCursor` | string |  |

## Native endpoint

Through the native Fathom API, this operation is `GET /meetings` (base URL `https://api.fathom.ai/external/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-meetings.md) for the provider-specific parameters and requirements.

