# Formitize: List Submitted Forms

Retrieves submitted forms from Formitize.

```
GET https://connect.mindcloud.co/v1/universal/formitize/latest/actions/list-submitted-forms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Formitize `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/formitize/latest/actions/list-submitted-forms?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/formitize/latest/actions/list-submitted-forms?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "count": "string",
      "dateCreated": 1,
      "dateModified": 1,
      "dateSubmitted": 1,
      "formDataLastSaved": 1,
      "formID": 1,
      "jobID": 1,
      "status": "string",
      "submittedFormID": 1,
      "title": "string",
      "userID": 1,
      "userName": "Ava Chen",
      "version": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | string |  |
| `dateCreated` | number |  |
| `dateModified` | number |  |
| `dateSubmitted` | number |  |
| `formDataLastSaved` | number |  |
| `formID` | number |  |
| `jobID` | number |  |
| `status` | string |  |
| `submittedFormID` | number |  |
| `title` | string |  |
| `userID` | number |  |
| `userName` | string |  |
| `version` | number |  |

## Native endpoint

Through the native Formitize API, this operation is `GET /form/submit/list` (base URL `https://service.formitize.com/api/rest/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-submitted-forms.md) for the provider-specific parameters and requirements.

