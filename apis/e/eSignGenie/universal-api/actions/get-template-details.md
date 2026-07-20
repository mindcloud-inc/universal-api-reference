# eSign Genie: Get Template Details

Retrieves template details from eSign Genie.

```
GET https://connect.mindcloud.co/v1/universal/eSignGenie/latest/actions/get-template-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eSign Genie `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eSignGenie/latest/actions/get-template-details?connectionId=$CONNECTION_ID&folderId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "folderId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eSignGenie/latest/actions/get-template-details?${params}`, {
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
| `folderId` | number | yes | The Foxit eSign template ID to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "allFields": [
        {
          "fieldTagId": 1,
          "fieldType": "string",
          "partyResponsible": 1
        }
      ],
      "result": "string",
      "template": {
        "companyId": 1,
        "numberOfParties": 1,
        "shareAll": true,
        "templateId": 1,
        "templateName": "Ava Chen"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allFields[].fieldTagId` | number |  |
| `allFields[].fieldType` | string |  |
| `allFields[].partyResponsible` | number |  |
| `result` | string |  |
| `template.companyId` | number |  |
| `template.numberOfParties` | number |  |
| `template.shareAll` | boolean |  |
| `template.templateId` | number |  |
| `template.templateName` | string |  |

## Native endpoint

Through the native eSign Genie API, this operation is `GET /templates/mytemplate` (base URL `https://na1.foxitesign.foxit.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-template-details.md) for the provider-specific parameters and requirements.

