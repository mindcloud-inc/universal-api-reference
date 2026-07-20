# SparkPost: Preview Template



```
GET https://connect.mindcloud.co/v1/universal/sparkPost/latest/actions/preview-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SparkPost `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sparkPost/latest/actions/preview-template?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sparkPost/latest/actions/preview-template?${params}`, {
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
| `id` | string | yes | Template identifier. |
| `substitutionData` | object | no | Data passed to the template engine while previewing. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "from": {},
      "html": "string",
      "subject": "string",
      "text": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `from` | object |  |
| `html` | string |  |
| `subject` | string |  |
| `text` | string |  |

## Native endpoint

Through the native SparkPost API, this operation is `POST /templates/:id/preview` (base URL `https://api.sparkpost.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/preview-template.md) for the provider-specific parameters and requirements.

