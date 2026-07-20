# Imagior: List Template Elements

Retrieves template elements from Imagior.

```
GET https://connect.mindcloud.co/v1/universal/imagior/latest/actions/list-template-elements
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Imagior `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/imagior/latest/actions/list-template-elements?connectionId=$CONNECTION_ID&templateId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "templateId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/imagior/latest/actions/list-template-elements?${params}`, {
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
| `templateId` | string | yes | The ID of the design template. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "elements": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `elements` | object | Map of element names to full element properties. |

## Native endpoint

Through the native Imagior API, this operation is `GET /templates/{templateId}/elements` (base URL `https://api.imagior.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-template-elements.md) for the provider-specific parameters and requirements.

