# Pirsonal: List Template Videos

Retrieves videos created from a Pirsonal template.

```
GET https://connect.mindcloud.co/v1/universal/pirsonal/latest/actions/list-template-videos
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pirsonal `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pirsonal/latest/actions/list-template-videos?connectionId=$CONNECTION_ID&templateID=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "templateID": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pirsonal/latest/actions/list-template-videos?${params}`, {
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
| `templateID` | string | yes | Template ID whose videos should be listed. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "analytics": {},
      "data": "string",
      "date": "string",
      "description": "string",
      "duration": 1,
      "email": "ava@example.com",
      "firstName": "Ava",
      "formData": [
        "string"
      ],
      "GATrackingCode": "string",
      "id": "string",
      "inputMedias": [
        {}
      ],
      "inputVariables": [
        {}
      ],
      "keywords": "string",
      "landingInfo": {},
      "lastName": "Chen",
      "name": "Ava Chen",
      "outFiles": [
        {}
      ],
      "playerInfo": {},
      "poweredbyPirsonalLogo": true,
      "status": {},
      "template_media": "string",
      "template_type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `analytics` | object | Video analytics. |
| `data` | string | User-attached video data. |
| `date` | string | Video creation date. |
| `description` | string | Video description. |
| `duration` | number | Video duration. |
| `email` | string | Email associated with the video. |
| `firstName` | string | Contact first name associated with the video. |
| `formData` | array<string> | Video form data. |
| `GATrackingCode` | string | Google Analytics tracking code. |
| `id` | string | Video ID. |
| `inputMedias` | array<object> | Input media allowed for the video. |
| `inputVariables` | array<object> | Input variables. |
| `keywords` | string | Comma-separated keywords. |
| `landingInfo` | object | Landing page information. |
| `lastName` | string | Contact last name associated with the video. |
| `name` | string | Video name. |
| `outFiles` | array<object> | Output files. |
| `playerInfo` | object | Player information. |
| `poweredbyPirsonalLogo` | boolean | Whether the Pirsonal logo is removed. |
| `status` | object | Video processing status. |
| `template_media` | string | Template media. |
| `template_type` | string | Template type. |

## Native endpoint

Through the native Pirsonal API, this operation is `POST /api` (base URL `https://app.pirsonal.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-template-videos.md) for the provider-specific parameters and requirements.

