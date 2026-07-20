# edatalia Sign Online: Get Envelope Evidence Document

Retrieves an envelope evidence document from edatalia Sign Online.

```
GET https://connect.mindcloud.co/v1/universal/edataliaSignOnline/latest/actions/get-envelope-evidence-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a edatalia Sign Online `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/edataliaSignOnline/latest/actions/get-envelope-evidence-document?connectionId=$CONNECTION_ID&documentSetId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "documentSetId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/edataliaSignOnline/latest/actions/get-envelope-evidence-document?${params}`, {
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
| `documentSetId` | string | yes | Identifier of the envelope whose evidence document should be retrieved. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content` | string | Evidence document content returned by the API. |

## Native endpoint

Through the native edatalia Sign Online API, this operation is `GET /PSC/v40/DocumentSet/Evidences/:documentSetId` (base URL `https://restapi.firmar.online`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-envelope-evidence-document.md) for the provider-specific parameters and requirements.

