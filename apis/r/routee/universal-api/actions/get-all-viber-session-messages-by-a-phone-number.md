# Routee: Get all Viber Session Messages by a Phone Number

Retrieves all Viber session messages by a phone number from Routee.

```
GET https://connect.mindcloud.co/v1/universal/routee/latest/actions/get-all-viber-session-messages-by-a-phone-number
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Routee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/routee/latest/actions/get-all-viber-session-messages-by-a-phone-number?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/routee/latest/actions/get-all-viber-session-messages-by-a-phone-number?${params}`, {
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
| `page` | number | no | The page number to retrieve, default value is 0 (meaning the first page). |
| `size` | number | no | The number of items to retrieve, default value is 20. |
| `phoneNumber` | string | no | The phone number. Format with a '+' and country code e.g., +3069485xxxxx (E.164 format). |
| `dateStart` | date | no | The start date of the query. |
| `dateEnd` | date | no | The end date of the query. Sessions will be included in their whole even if they exceed the end date set by the user. We will never return sessions with missing messages. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content": [
        [
          {}
        ]
      ],
      "first": true,
      "last": true,
      "number": 1,
      "numberOfElements": 1,
      "size": 1,
      "totalElements": 1,
      "totalPages": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content[]` | array<object> |  |
| `content[].sessionId` | string |  |
| `content[].sessionMessages[]` | array<object> |  |
| `content[].sessionMessages[].applicationName` | string |  |
| `content[].sessionMessages[].country` | string |  |
| `content[].sessionMessages[].direction` | string |  |
| `content[].sessionMessages[].file` | object |  |
| `content[].sessionMessages[].file.fileName` | string |  |
| `content[].sessionMessages[].file.fileType` | string |  |
| `content[].sessionMessages[].file.fileUrl` | string |  |
| `content[].sessionMessages[].from` | string |  |
| `content[].sessionMessages[].imageUrl` | string |  |
| `content[].sessionMessages[].message` | string |  |
| `content[].sessionMessages[].price` | number |  |
| `content[].sessionMessages[].status` | object |  |
| `content[].sessionMessages[].status.date` | string |  |
| `content[].sessionMessages[].status.reason` | object |  |
| `content[].sessionMessages[].status.reason.description` | string |  |
| `content[].sessionMessages[].status.reason.detailedStatus` | string |  |
| `content[].sessionMessages[].status.status` | string |  |
| `content[].sessionMessages[].to` | string |  |
| `content[].sessionMessages[].trackingId` | string |  |
| `content[].sessionMessages[].ttl` | string |  |
| `first` | boolean |  |
| `last` | boolean |  |
| `number` | number |  |
| `numberOfElements` | number |  |
| `size` | number |  |
| `totalElements` | number |  |
| `totalPages` | number |  |

## Native endpoint

Through the native Routee API, this operation is `POST /viber/session` (base URL `https://connect.routee.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-all-viber-session-messages-by-a-phone-number.md) for the provider-specific parameters and requirements.

