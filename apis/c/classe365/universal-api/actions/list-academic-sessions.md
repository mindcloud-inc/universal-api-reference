# Classe365: List Academic Sessions

Retrieves a list of academic sessions from Classe365.

```
GET https://connect.mindcloud.co/v1/universal/classe365/latest/actions/list-academic-sessions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Classe365 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/classe365/latest/actions/list-academic-sessions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/classe365/latest/actions/list-academic-sessions?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "academicSessionId": "string",
      "academicSessionName": "Ava Chen",
      "endDate": "2026-05-07T12:00:00.000Z",
      "startDate": "2026-05-07T12:00:00.000Z",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `academicSessionId` | string |  |
| `academicSessionName` | string |  |
| `endDate` | date |  |
| `startDate` | date |  |
| `status` | string |  |

## Native endpoint

Through the native Classe365 API, this operation is `GET /rest/academicSessions` (base URL `https://{{credentials.username}}.classe365.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-academic-sessions.md) for the provider-specific parameters and requirements.

