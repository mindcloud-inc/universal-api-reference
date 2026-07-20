# SafetyCulture: Retrieve Selected Media

Retrieves selected inspection media from SafetyCulture.

```
GET https://connect.mindcloud.co/v1/universal/safetyCulture/latest/actions/retrieve-selected-media
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SafetyCulture `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/safetyCulture/latest/actions/retrieve-selected-media?connectionId=$CONNECTION_ID&auditId=string&mediaId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "auditId": "string",
  "mediaId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/safetyCulture/latest/actions/retrieve-selected-media?${params}`, {
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
| `auditId` | string | yes | The id of the inspection to retrieve media from. |
| `mediaId` | string | yes | The id of the media to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "value": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | object |  |

## Native endpoint

Through the native SafetyCulture API, this operation is `GET /audits/{audit_id}/media/{media_id}` (base URL `https://api.safetyculture.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-selected-media.md) for the provider-specific parameters and requirements.

