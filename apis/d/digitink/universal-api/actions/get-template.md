# Digit.ink: Get Template



```
GET https://connect.mindcloud.co/v1/universal/digitink/latest/actions/get-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Digit.ink `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/digitink/latest/actions/get-template?connectionId=$CONNECTION_ID&templateUuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "templateUuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/digitink/latest/actions/get-template?${params}`, {
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
| `templateUuid` | string | yes | Template UUID path parameter. |

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

Through the native Digit.ink API, this operation is `GET /templates/:templateUuid` (base URL `https://app.digit.ink/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-template.md) for the provider-specific parameters and requirements.

