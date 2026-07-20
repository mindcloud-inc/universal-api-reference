# Leadspicker: List Inbound Messages

Retrieves inbound messages from Leadspicker.

```
GET https://connect.mindcloud.co/v1/universal/leadspicker/latest/actions/list-inbound-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Leadspicker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/leadspicker/latest/actions/list-inbound-messages?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/leadspicker/latest/actions/list-inbound-messages?${params}`, {
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
| `searchQuery` | string | no | Search in person name, email, subject, and message content. |
| `customStartDate` | date | no | Filter conversations received on or after this date (YYYY-MM-DD). |
| `customEndDate` | date | no | Filter conversations received on or before this date (YYYY-MM-DD). |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `browserTimezone` | string | no | IANA timezone name used for date boundaries. Example: `America/New_York`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "items": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `items` | array<object> |  |

## Native endpoint

Through the native Leadspicker API, this operation is `GET /app/sb/api/inbound-messages` (base URL `https://app.leadspicker.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-inbound-messages.md) for the provider-specific parameters and requirements.

