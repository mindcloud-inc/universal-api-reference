# Google Mail: Get Filter

Retrieves a filter from Gmail settings.

```
GET https://connect.mindcloud.co/v1/universal/gmail/latest/actions/get-filter
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Mail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gmail/latest/actions/get-filter?connectionId=$CONNECTION_ID&id=1234567890" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1234567890"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gmail/latest/actions/get-filter?${params}`, {
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
| `id` | string | yes | Filter ID to fetch. Example: `1234567890`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "criteria": {
        "from": "string",
        "subject": "string",
        "to": "string"
      },
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `criteria.from` | string |  |
| `criteria.subject` | string |  |
| `criteria.to` | string |  |
| `id` | string |  |

## Native endpoint

Through the native Google Mail API, this operation is `GET /settings/filters/:id` (base URL `https://gmail.googleapis.com/gmail/v1/users/:userId`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-filter.md) for the provider-specific parameters and requirements.

