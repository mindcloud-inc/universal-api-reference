# Remindlo: List Contacts



```
GET https://connect.mindcloud.co/v1/universal/remindlo/latest/actions/list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Remindlo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/remindlo/latest/actions/list-contacts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/remindlo/latest/actions/list-contacts?${params}`, {
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
| `createdAfter` | date | no |  |
| `hasPhone` | boolean | no |  |
| `isRecurrent` | boolean | no |  |
| `limit` | number | no | Default: `50`. |
| `marketingConsent` | boolean | no |  |
| `nextDueAfter` | date | no |  |
| `nextDueBefore` | date | no |  |
| `offset` | number | no |  |
| `search` | string | no |  |
| `sortBy` | string | no |  |
| `sortOrder` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contacts": [
        {}
      ],
      "pagination": {},
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contacts` | array<object> |  |
| `pagination` | object |  |
| `success` | boolean |  |

## Native endpoint

Through the native Remindlo API, this operation is `GET /contacts` (base URL `https://api.remindlo.co.uk/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contacts.md) for the provider-specific parameters and requirements.

