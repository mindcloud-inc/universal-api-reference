# Cliengo: Get Contact



```
GET https://connect.mindcloud.co/v1/universal/cliengo/latest/actions/get-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cliengo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cliengo/latest/actions/get-contact?connectionId=$CONNECTION_ID&contactId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contactId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cliengo/latest/actions/get-contact?${params}`, {
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
| `contactId` | string | yes | Identifier of the Cliengo contact. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": "string",
      "accountName": "Ava Chen",
      "age": 1,
      "calls": [
        "string"
      ],
      "creationDate": "2026-05-07T12:00:00.000Z",
      "duplicatedContact": true,
      "email": "ava@example.com",
      "entryMethod": "string",
      "geoip": {},
      "id": "string",
      "lastName": "Chen",
      "lastUpdateDate": "2026-05-07T12:00:00.000Z",
      "leadFields": {},
      "logs": [
        "string"
      ],
      "medium": "string",
      "mediumTranslate": "string",
      "message": "string",
      "name": "Ava Chen",
      "notes": [
        "string"
      ],
      "phone": "string",
      "rating": 1,
      "status": "string",
      "subStatus": "string",
      "utmCampaign": "string",
      "utmContent": "string",
      "utmMedium": "string",
      "utmTerm": "string",
      "websiteId": "string",
      "websiteName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | string |  |
| `accountName` | string |  |
| `age` | number |  |
| `calls` | array |  |
| `creationDate` | date |  |
| `duplicatedContact` | boolean |  |
| `email` | string |  |
| `entryMethod` | string |  |
| `geoip` | object |  |
| `id` | string |  |
| `lastName` | string |  |
| `lastUpdateDate` | date |  |
| `leadFields` | object |  |
| `logs` | array |  |
| `medium` | string |  |
| `mediumTranslate` | string |  |
| `message` | string |  |
| `name` | string |  |
| `notes` | array |  |
| `phone` | string |  |
| `rating` | number |  |
| `status` | string |  |
| `subStatus` | string |  |
| `utmCampaign` | string |  |
| `utmContent` | string |  |
| `utmMedium` | string |  |
| `utmTerm` | string |  |
| `websiteId` | string |  |
| `websiteName` | string |  |

## Native endpoint

Through the native Cliengo API, this operation is `GET /contacts/:contactId` (base URL `https://api.cliengo.com/1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact.md) for the provider-specific parameters and requirements.

