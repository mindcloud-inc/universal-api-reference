# IntakeQ: Query Treatment Notes

Retrieves treatment notes from IntakeQ.

```
GET https://connect.mindcloud.co/v1/universal/intakeQ/latest/actions/query-treatment-notes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a IntakeQ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/intakeQ/latest/actions/query-treatment-notes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/intakeQ/latest/actions/query-treatment-notes?${params}`, {
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
      "clientEmail": "ava@example.com",
      "clientId": 1,
      "clientName": "Ava Chen",
      "date": 1,
      "id": "string",
      "noteName": "Ava Chen",
      "practitionerEmail": "ava@example.com",
      "practitionerId": "string",
      "practitionerName": "Ava Chen",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `clientEmail` | string |  |
| `clientId` | number |  |
| `clientName` | string |  |
| `date` | number |  |
| `id` | string |  |
| `noteName` | string |  |
| `practitionerEmail` | string |  |
| `practitionerId` | string |  |
| `practitionerName` | string |  |
| `status` | string |  |

## Native endpoint

Through the native IntakeQ API, this operation is `GET /notes/summary` (base URL `https://intakeq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/query-treatment-notes.md) for the provider-specific parameters and requirements.

