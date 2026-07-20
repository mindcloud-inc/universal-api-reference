# IntakeQ: Get Client Diagnoses

Retrieves client diagnoses from IntakeQ.

```
GET https://connect.mindcloud.co/v1/universal/intakeQ/latest/actions/get-client-diagnoses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a IntakeQ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/intakeQ/latest/actions/get-client-diagnoses?connectionId=$CONNECTION_ID&clientId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "clientId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/intakeQ/latest/actions/get-client-diagnoses?${params}`, {
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
| `clientId` | string | yes | The IntakeQ numeric client ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "date": "string",
      "description": "string",
      "endDate": "string",
      "noteId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string |  |
| `date` | string |  |
| `description` | string |  |
| `endDate` | string |  |
| `noteId` | string |  |

## Native endpoint

Through the native IntakeQ API, this operation is `GET /client/{clientId}/diagnoses` (base URL `https://intakeq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-client-diagnoses.md) for the provider-specific parameters and requirements.

