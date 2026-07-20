# ModelsLab: List Uploaded Voices

Retrieves uploaded voices from ModelsLab.

```
GET https://connect.mindcloud.co/v1/universal/modelsLab/latest/actions/list-uploaded-voices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ModelsLab `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/modelsLab/latest/actions/list-uploaded-voices?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/modelsLab/latest/actions/list-uploaded-voices?${params}`, {
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
| `type` | string | no | Voice list type: manual, trained, or voice_cover. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": "string",
      "voices": [
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
| `status` | string |  |
| `voices` | array<object> |  |

## Native endpoint

Through the native ModelsLab API, this operation is `POST /v6/voice/voice_list` (base URL `https://modelslab.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-uploaded-voices.md) for the provider-specific parameters and requirements.

