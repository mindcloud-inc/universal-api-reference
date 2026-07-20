# Webex: Get Team

Retrieves a specific team from Webex.

```
GET https://connect.mindcloud.co/v1/universal/webex/latest/actions/get-team
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Webex `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/webex/latest/actions/get-team?connectionId=$CONNECTION_ID&teamId=Y2lzY29zcGFyazovL3VzL1RFQU0v..." \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "teamId": "Y2lzY29zcGFyazovL3VzL1RFQU0v..."
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/webex/latest/actions/get-team?${params}`, {
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
| `teamId` | string | yes | Team identifier. Example: `Y2lzY29zcGFyazovL3VzL1RFQU0v...`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": "2026-05-07T12:00:00.000Z",
      "creatorId": "string",
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | date | Team creation timestamp. |
| `creatorId` | string | Person identifier for the team creator. |
| `id` | string | Team identifier. |
| `name` | string | Team name. |

## Native endpoint

Through the native Webex API, this operation is `GET /teams/:teamId` (base URL `https://webexapis.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-team.md) for the provider-specific parameters and requirements.

