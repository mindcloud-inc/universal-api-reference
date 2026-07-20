# Formitize: Get Submitted Form

Retrieves a submitted form from Formitize.

```
GET https://connect.mindcloud.co/v1/universal/formitize/latest/actions/get-submitted-form
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Formitize `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/formitize/latest/actions/get-submitted-form?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/formitize/latest/actions/get-submitted-form?${params}`, {
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
| `id` | string | no | Formitize submitted form ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attachments": {},
      "content": {},
      "count": "string",
      "dateModified": "string",
      "dateSubmitted": "string",
      "formDataLastSaved": "string",
      "formDateCreated": "string",
      "formID": "string",
      "jobID": "string",
      "modifiedBy": "string",
      "status": "string",
      "submittedFormID": "string",
      "title": "string",
      "userID": "string",
      "userName": "Ava Chen",
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attachments` | object |  |
| `content` | object |  |
| `count` | string |  |
| `dateModified` | string |  |
| `dateSubmitted` | string |  |
| `formDataLastSaved` | string |  |
| `formDateCreated` | string |  |
| `formID` | string |  |
| `jobID` | string |  |
| `modifiedBy` | string |  |
| `status` | string |  |
| `submittedFormID` | string |  |
| `title` | string |  |
| `userID` | string |  |
| `userName` | string |  |
| `version` | string |  |

## Native endpoint

Through the native Formitize API, this operation is `GET /form/submit/:id` (base URL `https://service.formitize.com/api/rest/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-submitted-form.md) for the provider-specific parameters and requirements.

