# Documo: Send Fax

Creates a new fax message in Documo.

```
POST https://connect.mindcloud.co/v1/universal/documo/latest/actions/send-fax
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Documo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/documo/latest/actions/send-fax" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "faxNumber": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/documo/latest/actions/send-fax', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "faxNumber": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `faxNumber` | string | yes | String \| Required \| Destination phone number |
| `coverPage` | boolean | no | Boolean \| Include system cover page; removes file requirement when true |
| `coverPageId` | string | no | UUID \| Cover page UUID to include |
| `tags` | string | no | String \| Comma separated list of tag IDs |
| `recipientName` | string | no | String \| 40 character limit |
| `senderName` | string | no | String \| 40 character limit |
| `subject` | string | no | String \| 55 character limit |
| `callerId` | string | no | String \| 10 character limit \| Phone number |
| `notes` | string | no | String \| 4000 character limit |
| `cf` | string | no | String \| JSON object with custom fields |
| `scheduledDate` | string | no | String \| ISO date-time for scheduled send |
| `attachments` | file | no | File \| Required if coverPage is not added |
| `attachmentUrls` | string | no | String \| URL list for attached documents |
| `fileIds` | string | no | String \| UUID list of mDrive file entities |
| `async` | boolean | no | Boolean \| When true, immediately returns only messageId |
| `optimizeFax` | string | no | String \| auto, text, or image |

## Response

```json
{
  "success": true,
  "data": [
    {
      "account": {
        "accountName": "Ava Chen",
        "accountType": "string",
        "uuid": "string"
      },
      "accountId": "string",
      "channelType": "string",
      "classificationLabel": "string",
      "country": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "direction": "string",
      "faxCallerId": "string",
      "faxCsid": "string",
      "faxNumber": "string",
      "isArchived": true,
      "isFilePurged": true,
      "messageId": "string",
      "pagesComplete": 1,
      "pagesCount": 1,
      "processingStatusName": "Ava Chen",
      "resultCode": "string",
      "resultInfo": "string",
      "status": "string",
      "users": [
        {
          "email": "ava@example.com",
          "firstName": "Ava",
          "lastName": "Chen",
          "userId": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account.accountName` | string |  |
| `account.accountType` | string |  |
| `account.uuid` | string |  |
| `accountId` | string |  |
| `channelType` | string |  |
| `classificationLabel` | string |  |
| `country` | string |  |
| `createdAt` | date |  |
| `direction` | string |  |
| `faxCallerId` | string |  |
| `faxCsid` | string |  |
| `faxNumber` | string |  |
| `isArchived` | boolean |  |
| `isFilePurged` | boolean |  |
| `messageId` | string |  |
| `pagesComplete` | number |  |
| `pagesCount` | number |  |
| `processingStatusName` | string |  |
| `resultCode` | string |  |
| `resultInfo` | string |  |
| `status` | string |  |
| `users[].email` | string |  |
| `users[].firstName` | string |  |
| `users[].lastName` | string |  |
| `users[].userId` | string |  |

## Native endpoint

Through the native Documo API, this operation is `POST /v1/faxes` (base URL `https://api.documo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-fax.md) for the provider-specific parameters and requirements.

