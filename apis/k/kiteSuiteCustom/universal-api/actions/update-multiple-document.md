# Kite Suite: Update multiple document



```
PUT https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/update-multiple-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kite Suite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/update-multiple-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "body": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/update-multiple-document', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "body": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `body` | object | yes | Request body |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_id": "string",
      "access": {},
      "childNodes": [
        "string"
      ],
      "documentName": "Ava Chen",
      "file": {},
      "isTrashed": true,
      "owner": "string",
      "pages": [
        "string"
      ],
      "parentNodes": [
        "string"
      ],
      "peoples": [
        "string"
      ],
      "project": "string",
      "shareWithAnyone": [
        "string"
      ],
      "starredDoc": [
        "string"
      ],
      "type": "string",
      "workspace": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string | ID of the Document |
| `access` | object |  |
| `childNodes` | array | array of pages |
| `documentName` | string | title of document |
| `file` | object |  |
| `isTrashed` | boolean | trash status of this document |
| `owner` | string | owner of the this Document |
| `pages` | array |  |
| `parentNodes` | array | array of documents |
| `peoples` | array |  |
| `project` | string | project ID of project |
| `shareWithAnyone` | array | array of users |
| `starredDoc` | array |  |
| `type` | string | title of document |
| `workspace` | string | ID of workspace |

## Native endpoint

Through the native Kite Suite API, this operation is `POST /api/v1/document/multiple` (base URL `https://api.kitesuite.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-multiple-document.md) for the provider-specific parameters and requirements.

