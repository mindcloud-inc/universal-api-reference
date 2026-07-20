# Google Slides: Get Page

Retrieves a presentation page from Google Slides.

```
GET https://connect.mindcloud.co/v1/universal/googleSlides/latest/actions/get-page
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Slides `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleSlides/latest/actions/get-page?connectionId=$CONNECTION_ID&presentationId=string&pageObjectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "presentationId": "string",
  "pageObjectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleSlides/latest/actions/get-page?${params}`, {
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
| `presentationId` | string | yes | The ID of the presentation. |
| `pageObjectId` | string | yes | The object ID of the page to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "objectId": "string",
      "pageElements": [
        {}
      ],
      "pageProperties": {},
      "revisionId": "string",
      "slideProperties": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `objectId` | string | The object ID of the page. |
| `pageElements` | array<object> | The elements contained on the page. |
| `pageProperties` | object | The page-level properties. |
| `revisionId` | string | The revision ID for the page. |
| `slideProperties` | object | The slide-level properties for the page. |

## Native endpoint

Through the native Google Slides API, this operation is `GET /v1/presentations/:presentationId/pages/:pageObjectId` (base URL `https://slides.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-page.md) for the provider-specific parameters and requirements.

