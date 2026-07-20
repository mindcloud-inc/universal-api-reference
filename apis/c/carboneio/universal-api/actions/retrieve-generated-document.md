# Carbone.io: Retrieve Generated Document

Downloads a generated document from Carbone.io.

```
GET https://connect.mindcloud.co/v1/universal/carboneio/latest/actions/retrieve-generated-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Carbone.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/carboneio/latest/actions/retrieve-generated-document?connectionId=$CONNECTION_ID&renderId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "renderId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/carboneio/latest/actions/retrieve-generated-document?${params}`, {
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
| `renderId` | string | yes | Render ID returned by a previous generate or convert request. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | string | Raw generated document bytes returned by Carbone. |

## Native endpoint

Through the native Carbone.io API, this operation is `GET /render/:renderId` (base URL `https://api.carbone.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-generated-document.md) for the provider-specific parameters and requirements.

