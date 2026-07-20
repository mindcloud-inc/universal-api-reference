# Casting42: List Talent Audios

Retrieves audio files for a Casting42 talent.

```
GET https://connect.mindcloud.co/v1/universal/casting42/latest/actions/list-talent-audios
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Casting42 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/casting42/latest/actions/list-talent-audios?connectionId=$CONNECTION_ID&talentTag=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "talentTag": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/casting42/latest/actions/list-talent-audios?${params}`, {
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
| `talentTag` | string | yes | Unique tag of the talent whose audio files you want to fetch. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attachmentLabel": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "filename": "Ava Chen",
      "tag": "string",
      "talentTag": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attachmentLabel` | string | Attachment label. |
| `createdAt` | date | Audio creation timestamp. |
| `filename` | string | Audio filename. |
| `tag` | string | Audio attachment tag. |
| `talentTag` | string | Related talent tag. |
| `url` | string | Audio download URL. |

## Native endpoint

Through the native Casting42 API, this operation is `GET /api/v2/talents/audios/{{talentTag}}` (base URL `https://casting42.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-talent-audios.md) for the provider-specific parameters and requirements.

