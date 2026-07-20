# eSign Genie: Get Envelope Details

Retrieves envelope details from eSign Genie.

```
GET https://connect.mindcloud.co/v1/universal/eSignGenie/latest/actions/get-envelope-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eSign Genie `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eSignGenie/latest/actions/get-envelope-details?connectionId=$CONNECTION_ID&folderId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "folderId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eSignGenie/latest/actions/get-envelope-details?${params}`, {
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
| `folderId` | number | yes | The Foxit eSign envelope ID to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "allFields": [
        {
          "fieldTagId": 1,
          "fieldType": "string"
        }
      ],
      "folder": {
        "documentsList": [
          {
            "documentId": 1
          }
        ],
        "envelopeStatus": "string",
        "folderDocumentIds": [
          1
        ],
        "folderId": 1,
        "folderName": "Ava Chen",
        "folderRecipientParties": [
          {
            "partyId": 1
          }
        ],
        "folderStatus": "string"
      },
      "result": "string"
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
| `folder.documentsList[].documentId` | number |  |
| `folder.envelopeStatus` | string |  |
| `folder.folderDocumentIds[]` | number |  |
| `folder.folderId` | number |  |
| `folder.folderName` | string |  |
| `folder.folderRecipientParties[].partyId` | number |  |
| `folder.folderStatus` | string |  |
| `result` | string |  |

## Native endpoint

Through the native eSign Genie API, this operation is `GET /folders/myfolder` (base URL `https://na1.foxitesign.foxit.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-envelope-details.md) for the provider-specific parameters and requirements.

