# CoachAccountable: List Sessions

Retrieves sessions from CoachAccountable.

```
GET https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/list-sessions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CoachAccountable `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/list-sessions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/list-sessions?${params}`, {
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
| `clientId` | number | no | Filter Sessions by Client. |
| `dateFrom` | date | no | Set to restrict Sessions returned to those at or after the provided value. |
| `dateTo` | date | no | Set to restrict Sessions returned to those at or before the provided value. |
| `includeDrafts` | boolean | no | Set to true to include Sessions not yet marked complete. Default: `false`. |
| `sortField` | list | no | One of: `dateAdded`, `dateDone`, `dateOf`. Default: `dateDone`. |
| `sortDirection` | list | no | One of: `A`, `D`. Default: `D`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "answerSet": [
        {
          "name": "Ava Chen",
          "numberValue": 1,
          "value": "string"
        }
      ],
      "ClientID": 1,
      "CoachID": 1,
      "content": "string",
      "dateAdded": "2026-05-07T12:00:00.000Z",
      "dateDone": "2026-05-07T12:00:00.000Z",
      "dateOf": "2026-05-07T12:00:00.000Z",
      "ID": 1,
      "isDraft": true,
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `answerSet` | array<object> |  |
| `answerSet[].name` | string |  |
| `answerSet[].numberValue` | number |  |
| `answerSet[].value` | string |  |
| `ClientID` | number |  |
| `CoachID` | number |  |
| `content` | string |  |
| `dateAdded` | date |  |
| `dateDone` | date |  |
| `dateOf` | date |  |
| `ID` | number |  |
| `isDraft` | boolean |  |
| `title` | string |  |

## Native endpoint

Through the native CoachAccountable API, this operation is `POST /` (base URL `https://www.coachaccountable.com/API`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-sessions.md) for the provider-specific parameters and requirements.

