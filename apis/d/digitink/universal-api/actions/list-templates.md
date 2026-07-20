# Digit.ink: List Templates



```
GET https://connect.mindcloud.co/v1/universal/digitink/latest/actions/list-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Digit.ink `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/digitink/latest/actions/list-templates?connectionId=$CONNECTION_ID&key=credentialType&value=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "key": "credentialType",
  "value": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/digitink/latest/actions/list-templates?${params}`, {
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
| `key` | list | yes | Digit.ink template filter key. One of: `credentialType`, `name`, `templateUuid`. |
| `value` | string | yes | Digit.ink template filter value. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "credentialType": "string",
      "name": "Ava Chen",
      "templateStoragePath": "string",
      "thumbnailUrl": "https://example.com",
      "timeLastSaved": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `credentialType` | string |  |
| `name` | string |  |
| `templateStoragePath` | string |  |
| `thumbnailUrl` | string |  |
| `timeLastSaved` | date |  |

## Native endpoint

Through the native Digit.ink API, this operation is `GET /templates` (base URL `https://app.digit.ink/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-templates.md) for the provider-specific parameters and requirements.

