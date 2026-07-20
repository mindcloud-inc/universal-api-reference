# Mailform: Get All Teams



```
GET https://connect.mindcloud.co/v1/universal/mailform/latest/actions/get-all-teams
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mailform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailform/latest/actions/get-all-teams?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailform/latest/actions/get-all-teams?${params}`, {
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
      "data": [
        {
          "balance": {},
          "id": "string",
          "joined": "2026-05-07T12:00:00.000Z",
          "name": "Ava Chen",
          "object": "string",
          "owner": true
        }
      ],
      "object": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | Teams available to the authenticated user. |
| `data[].balance` | object | Prepaid account balance associated with the team. |
| `data[].id` | string | Team ID. |
| `data[].joined` | date | When the authenticated user joined the team. |
| `data[].name` | string | Team or company name. |
| `data[].object` | string | Team resource object type. |
| `data[].owner` | boolean | Whether the authenticated user is a team owner. |
| `object` | string | Envelope object type. |
| `success` | boolean | Whether the team list request succeeded. |

## Native endpoint

Through the native Mailform API, this operation is `GET /teams` (base URL `https://www.mailform.io/app/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-all-teams.md) for the provider-specific parameters and requirements.

