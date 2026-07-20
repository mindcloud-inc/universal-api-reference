# Zenvoices: Get Inbox Document

Retrieves an inbox document from your Zenvoices workspace.

```
GET https://connect.mindcloud.co/v1/universal/zenvoices/latest/actions/get-inbox-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zenvoices `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zenvoices/latest/actions/get-inbox-document?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zenvoices/latest/actions/get-inbox-document?${params}`, {
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
      "administrationId": 1,
      "authorizationStatus": 1,
      "destination": "string",
      "externalId": "string",
      "id": 1,
      "importStatus": 1,
      "receivedTime": "2026-05-07T12:00:00.000Z",
      "senderName": "Ava Chen",
      "subject": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `administrationId` | number | administrationId returned by Zenvoices. |
| `authorizationStatus` | number | authorizationStatus returned by Zenvoices. |
| `destination` | string | destination returned by Zenvoices. |
| `externalId` | string | externalId returned by Zenvoices. |
| `id` | number | id returned by Zenvoices. |
| `importStatus` | number | importStatus returned by Zenvoices. |
| `receivedTime` | date | receivedTime returned by Zenvoices. |
| `senderName` | string | senderName returned by Zenvoices. |
| `subject` | string | subject returned by Zenvoices. |

## Native endpoint

Through the native Zenvoices API, this operation is `GET /public-api/v1/inbox/details` (base URL `https://app.zenvoices.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-inbox-document.md) for the provider-specific parameters and requirements.

