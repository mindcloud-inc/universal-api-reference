# Flotiq: Get Media Version

Retrieves a media object version from Flotiq.

```
GET https://connect.mindcloud.co/v1/universal/flotiq/latest/actions/get-media-version
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Flotiq `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/flotiq/latest/actions/get-media-version?connectionId=$CONNECTION_ID&id=string&versionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string",
  "versionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/flotiq/latest/actions/get-media-version?${params}`, {
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
| `id` | string | yes | The Flotiq media object ID. |
| `versionId` | string | yes | The media version ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "current": true,
      "deletedAt": "2026-05-07T12:00:00.000Z",
      "editor": {},
      "id": "string",
      "internal": {},
      "owner": {},
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "version": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `current` | boolean |  |
| `deletedAt` | date |  |
| `editor` | object |  |
| `id` | string |  |
| `internal` | object |  |
| `owner` | object |  |
| `updatedAt` | date |  |
| `version` | number |  |

## Native endpoint

Through the native Flotiq API, this operation is `GET /content/_media/{{id}}/version/{{versionId}}` (base URL `https://api.flotiq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-media-version.md) for the provider-specific parameters and requirements.

