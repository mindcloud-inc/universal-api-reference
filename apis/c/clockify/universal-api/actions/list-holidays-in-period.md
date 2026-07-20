# Clockify: List Holidays in Period

Lists holidays in a period in Clockify.

```
GET https://connect.mindcloud.co/v1/universal/clockify/latest/actions/list-holidays-in-period
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clockify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clockify/latest/actions/list-holidays-in-period?connectionId=$CONNECTION_ID&workspaceId=string&assignedTo=string&end=2026-01-01&start=2026-01-01" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceId": "string",
  "assignedTo": "string",
  "end": "2026-01-01",
  "start": "2026-01-01"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clockify/latest/actions/list-holidays-in-period?${params}`, {
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
| `workspaceId` | list<string> | yes |  |
| `assignedTo` | string | yes |  |
| `end` | string | yes | Example: `2026-01-01`. |
| `start` | string | yes | Example: `2026-01-01`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "items": [
        [
          "string"
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `items[]` | array |  |

## Native endpoint

Through the native Clockify API, this operation is `GET workspaces/:workspaceId/holidays/in-period` (base URL `https://api.clockify.me/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-holidays-in-period.md) for the provider-specific parameters and requirements.

