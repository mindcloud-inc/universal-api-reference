# DocuPipe: List Classes

Retrieves classes from DocuPipe.

```
GET https://connect.mindcloud.co/v1/universal/docuPipe/latest/actions/list-classes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocuPipe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docuPipe/latest/actions/list-classes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docuPipe/latest/actions/list-classes?${params}`, {
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
| `includeUnknown` | boolean | no | Default: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "classId": "string",
      "className": "Ava Chen",
      "description": "string",
      "timestamp": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `classId` | string | Unique identifier of the classification object. |
| `className` | string | Name of the class. |
| `description` | string | Description of the class. |
| `timestamp` | string | Timestamp of the classification creation. |

## Native endpoint

Through the native DocuPipe API, this operation is `GET /classes` (base URL `https://app.docupipe.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-classes.md) for the provider-specific parameters and requirements.

