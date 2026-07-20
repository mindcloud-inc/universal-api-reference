# Channels: Get Contact History

Retrieves contact history from Channels.

```
GET https://connect.mindcloud.co/v1/universal/channels/latest/actions/get-contact-history
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Channels `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/channels/latest/actions/get-contact-history?connectionId=$CONNECTION_ID&contactId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contactId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/channels/latest/actions/get-contact-history?${params}`, {
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
| `contactId` | number | yes | Contact ID whose history should be returned. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "": [
        {
          "agentUsername": "Ava Chen",
          "appType": "string",
          "callerIdInfo": {
            "isoCountry": "string",
            "label": "string",
            "msisdn": "string"
          },
          "callId": 1,
          "callLength": 1,
          "clientMsisdn": "string",
          "contactId": 1,
          "createdAt": "2026-05-07T12:00:00.000Z",
          "customStatus": "string",
          "historicalCallerId": "string",
          "id": 1,
          "name": "Ava Chen",
          "newMsisdn": "string",
          "note": "string",
          "oldMsisdn": "string",
          "recordingAvailable": true,
          "surname": "Ava Chen",
          "type": "string"
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
| `[].agentUsername` | string |  |
| `[].appType` | string |  |
| `[].callerIdInfo.isoCountry` | string |  |
| `[].callerIdInfo.label` | string |  |
| `[].callerIdInfo.msisdn` | string |  |
| `[].callId` | number |  |
| `[].callLength` | number |  |
| `[].clientMsisdn` | string |  |
| `[].contactId` | number |  |
| `[].createdAt` | date |  |
| `[].customStatus` | string |  |
| `[].historicalCallerId` | string |  |
| `[].id` | number |  |
| `[].name` | string |  |
| `[].newMsisdn` | string |  |
| `[].note` | string |  |
| `[].oldMsisdn` | string |  |
| `[].recordingAvailable` | boolean |  |
| `[].surname` | string |  |
| `[].type` | string |  |

## Native endpoint

Through the native Channels API, this operation is `GET /api/v1/contacts/{contactId}/history` (base URL `https://api.channels.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact-history.md) for the provider-specific parameters and requirements.

