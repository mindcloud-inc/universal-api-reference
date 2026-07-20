# Kite Suite: Get page by page ID



```
GET https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/get-page-by-page-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kite Suite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/get-page-by-page-id?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/get-page-by-page-id?${params}`, {
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
| `id` | string | yes | Page ID |

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

Through the native Kite Suite API, this operation is `GET /api/v1/page/:id` (base URL `https://api.kitesuite.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-page-by-page-id.md) for the provider-specific parameters and requirements.

