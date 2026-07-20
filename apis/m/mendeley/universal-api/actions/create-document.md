# Mendeley: Create Document



```
POST https://connect.mindcloud.co/v1/universal/mendeley/latest/actions/create-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mendeley `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mendeley/latest/actions/create-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "How To Choose a Good Scientific Problem",
  "type": "journal"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mendeley/latest/actions/create-document', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "How To Choose a Good Scientific Problem",
    "type": "journal"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `title` | string | yes | Title of the document to create. Example: `How To Choose a Good Scientific Problem`. |
| `type` | list | yes | Document type. One of: `0`, `1`, `10`, `11`, `12`, `13`, `14`, `15`, `16`, `17`, `18`, `19`, `2`, `3`, `4`, `5`, `6`, `7`, `8`, `9`. Example: `journal`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": "string",
      "id": "string",
      "lastModified": "string",
      "profileId": "string",
      "title": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | string |  |
| `id` | string |  |
| `lastModified` | string |  |
| `profileId` | string |  |
| `title` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Mendeley API, this operation is `POST /documents` (base URL `https://api.mendeley.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-document.md) for the provider-specific parameters and requirements.

