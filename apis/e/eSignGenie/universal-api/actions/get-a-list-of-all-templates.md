# eSign Genie: Get a List of All Templates

Retrieves templates from eSign Genie.

```
GET https://connect.mindcloud.co/v1/universal/eSignGenie/latest/actions/get-a-list-of-all-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eSign Genie `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eSignGenie/latest/actions/get-a-list-of-all-templates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eSignGenie/latest/actions/get-a-list-of-all-templates?${params}`, {
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
| `templateId` | number | no | Optional template ID filter supported by the Foxit example request. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": "string",
      "templatesList": [
        {
          "companyId": 1,
          "editable": true,
          "numberOfParties": 1,
          "shareAll": true,
          "templateId": 1,
          "templateName": "Ava Chen",
          "templateType": "string"
        }
      ],
      "totalTemplates": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | string |  |
| `templatesList[].companyId` | number |  |
| `templatesList[].editable` | boolean |  |
| `templatesList[].numberOfParties` | number |  |
| `templatesList[].shareAll` | boolean |  |
| `templatesList[].templateId` | number |  |
| `templatesList[].templateName` | string |  |
| `templatesList[].templateType` | string |  |
| `totalTemplates` | number |  |

## Native endpoint

Through the native eSign Genie API, this operation is `GET /templates/list` (base URL `https://na1.foxitesign.foxit.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-a-list-of-all-templates.md) for the provider-specific parameters and requirements.

