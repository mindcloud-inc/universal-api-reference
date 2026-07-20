# Duply: Get Template Detail

Retrieves details for a Duply template.

```
GET https://connect.mindcloud.co/v1/universal/duply/latest/actions/get-template-detail
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Duply `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/duply/latest/actions/get-template-detail?connectionId=$CONNECTION_ID&templateId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "templateId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/duply/latest/actions/get-template-detail?${params}`, {
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
| `templateId` | string | yes | The ID of the template to fetch. |
| `variantName` | string | no | Optional template variant name. Defaults to the oldest variant when omitted. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content": {
        "height": 1,
        "variantName": "Ava Chen",
        "width": 1
      },
      "created": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "name": "Ava Chen",
      "updated": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content.height` | number |  |
| `content.variantName` | string |  |
| `content.width` | number |  |
| `created` | date |  |
| `id` | string |  |
| `name` | string |  |
| `updated` | date |  |

## Native endpoint

Through the native Duply API, this operation is `GET /template/:templateId` (base URL `https://gen.duply.co/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-template-detail.md) for the provider-specific parameters and requirements.

