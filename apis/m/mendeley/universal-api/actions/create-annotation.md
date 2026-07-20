# Mendeley: Create Annotation



```
POST https://connect.mindcloud.co/v1/universal/mendeley/latest/actions/create-annotation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mendeley `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mendeley/latest/actions/create-annotation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "documentId": "2531dfc9-90cd-3136-8001-abadb5929161",
  "filehash": "bd3293b2-d20c-0d9f-3773-df51a506c7b2",
  "positions[]": "[object Object]",
  "text": "Highlighted note text"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mendeley/latest/actions/create-annotation', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "documentId": "2531dfc9-90cd-3136-8001-abadb5929161",
    "filehash": "bd3293b2-d20c-0d9f-3773-df51a506c7b2",
    "positions[]": "[object Object]",
    "text": "Highlighted note text"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `documentId` | string | yes | ID of the document the annotation belongs to. Example: `2531dfc9-90cd-3136-8001-abadb5929161`. |
| `filehash` | string | yes | filehash of the file the annotation belongs to. Example: `bd3293b2-d20c-0d9f-3773-df51a506c7b2`. |
| `positions[]` | array<object> | yes | Annotation positions array as defined by the Mendeley API. Example: `[object Object]`. |
| `text` | string | yes | Annotation text content. Example: `Highlighted note text`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": "string",
      "documentId": "string",
      "filehash": "string",
      "id": "string",
      "lastModified": "string",
      "positions": [
        {
          "bottomRight": {
            "x": 1,
            "y": 1
          },
          "page": 1,
          "topLeft": {
            "x": 1,
            "y": 1
          }
        }
      ],
      "privacyLevel": "string",
      "profileId": "string",
      "text": "string",
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
| `documentId` | string |  |
| `filehash` | string |  |
| `id` | string |  |
| `lastModified` | string |  |
| `positions[].bottomRight.x` | number |  |
| `positions[].bottomRight.y` | number |  |
| `positions[].page` | number |  |
| `positions[].topLeft.x` | number |  |
| `positions[].topLeft.y` | number |  |
| `privacyLevel` | string |  |
| `profileId` | string |  |
| `text` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Mendeley API, this operation is `POST /annotations` (base URL `https://api.mendeley.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-annotation.md) for the provider-specific parameters and requirements.

