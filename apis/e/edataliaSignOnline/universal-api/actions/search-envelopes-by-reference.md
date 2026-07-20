# edatalia Sign Online: Search Envelopes By Reference

Finds envelopes in edatalia Sign Online by external reference.

```
GET https://connect.mindcloud.co/v1/universal/edataliaSignOnline/latest/actions/search-envelopes-by-reference
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a edatalia Sign Online `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/edataliaSignOnline/latest/actions/search-envelopes-by-reference?connectionId=$CONNECTION_ID&documentSetReference=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "documentSetReference": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/edataliaSignOnline/latest/actions/search-envelopes-by-reference?${params}`, {
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
| `documentSetReference` | string | yes | External envelope reference to search for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "creationDate": "2026-05-07T12:00:00.000Z",
      "documents": [
        {}
      ],
      "documentSetId": "string",
      "documentSetName": "Ava Chen",
      "documentSetReference": "string",
      "downloaded": true,
      "estimatedPurgationDate": "2026-05-07T12:00:00.000Z",
      "expirationDate": "2026-05-07T12:00:00.000Z",
      "expireDays": 1,
      "flowName": "Ava Chen",
      "flowTokenId": "string",
      "listDatesReminderDays": [
        "2026-05-07T12:00:00.000Z"
      ],
      "ltv": true,
      "purgated": true,
      "purgationDate": "2026-05-07T12:00:00.000Z",
      "recipients": [
        {}
      ],
      "reminderDays": 1,
      "senderMail": "string",
      "senderName": "Ava Chen",
      "sendMethod": 1,
      "status": 1,
      "statusTime": "2026-05-07T12:00:00.000Z",
      "teamId": "string",
      "teamName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `creationDate` | date | Date and time when the envelope was created. |
| `documents` | array<object> | Documents in the envelope, including document id, name, and hash when returned. |
| `documentSetId` | string | Unique identifier of the envelope. |
| `documentSetName` | string | Envelope name. |
| `documentSetReference` | string | Customer or external reference for the envelope. |
| `downloaded` | boolean | Whether the signed documents have been downloaded. |
| `estimatedPurgationDate` | date | Estimated date and time when documents may be purged. |
| `expirationDate` | date | Date and time when the envelope expires. |
| `expireDays` | number | Expiration timeout in days. |
| `flowName` | string | Flow name used to create the envelope, when present. |
| `flowTokenId` | string | Flow token identifier used to create the envelope, when present. |
| `listDatesReminderDays` | array<date> | Specific reminder dates for the envelope. |
| `ltv` | boolean | Whether long-term validation was requested. |
| `purgated` | boolean | Whether the envelope documents have been purged. |
| `purgationDate` | date | Date and time when the envelope documents were purged. |
| `recipients` | array<object> | Recipients in the envelope, including signer identity and action status details when returned. |
| `reminderDays` | number | Reminder interval in days. |
| `senderMail` | string | Email address of the envelope sender. |
| `senderName` | string | Name of the envelope sender. |
| `sendMethod` | number | Send method used for the envelope. |
| `status` | number | Envelope status code. |
| `statusTime` | date | Date and time when the envelope reached its current status. |
| `teamId` | string | Team identifier associated with the envelope. |
| `teamName` | string | Team name associated with the envelope. |

## Native endpoint

Through the native edatalia Sign Online API, this operation is `GET /PSC/v40/DocumentSet/InfoByReference/:documentSetReference` (base URL `https://restapi.firmar.online`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-envelopes-by-reference.md) for the provider-specific parameters and requirements.

