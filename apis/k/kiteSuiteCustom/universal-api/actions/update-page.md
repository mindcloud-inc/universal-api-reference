# Kite Suite: Update page



```
PUT https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/update-page
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kite Suite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/update-page" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "body": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/update-page', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "body": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Page ID |
| `body` | object | yes | Request body |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_id": "string",
      "activity": [
        "string"
      ],
      "attachment": "string",
      "author": "string",
      "description": "string",
      "docSettings": {},
      "document": "string",
      "headerImage": "string",
      "isTrashed": true,
      "linkDocs": [
        "https://example.com"
      ],
      "parentDoc": "string",
      "subDocs": [
        "string"
      ],
      "subTitle": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string | ID of the Page |
| `activity` | array | activity of Page |
| `attachment` | string | array of attachment |
| `author` | string | author of the this Page |
| `description` | string | Description of Page |
| `docSettings` | object |  |
| `document` | string | Document ID |
| `headerImage` | string | header image to Page |
| `isTrashed` | boolean | trash status of this task |
| `linkDocs` | array | link of Page |
| `parentDoc` | string | parent Page id of the Page |
| `subDocs` | array | array of sub Page |
| `subTitle` | string | sub title of Page |
| `title` | string | title of Page |

## Native endpoint

Through the native Kite Suite API, this operation is `PATCH /api/v1/page/:id` (base URL `https://api.kitesuite.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-page.md) for the provider-specific parameters and requirements.

