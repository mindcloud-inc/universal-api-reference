# Digital Samba: Download the specified recording

Retrieves a recording download from Digital Samba.

```
GET https://connect.mindcloud.co/v1/universal/digitalSamba/latest/actions/download-the-specified-recording
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Digital Samba `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/digitalSamba/latest/actions/download-the-specified-recording?connectionId=$CONNECTION_ID&recording=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "recording": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/digitalSamba/latest/actions/download-the-specified-recording?${params}`, {
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
| `recording` | string | yes | Recording path parameter. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `validForMinutes` | number | no | Link expiration time in minutes. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "link": "https://example.com",
      "validUntil": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `link` | string |  |
| `validUntil` | string |  |

## Native endpoint

Through the native Digital Samba API, this operation is `GET /recordings/:recording/download` (base URL `https://api.digitalsamba.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-the-specified-recording.md) for the provider-specific parameters and requirements.

