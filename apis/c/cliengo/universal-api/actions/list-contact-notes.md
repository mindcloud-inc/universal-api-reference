# Cliengo: List Contact Notes



```
GET https://connect.mindcloud.co/v1/universal/cliengo/latest/actions/list-contact-notes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cliengo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cliengo/latest/actions/list-contact-notes?connectionId=$CONNECTION_ID&contactId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contactId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cliengo/latest/actions/list-contact-notes?${params}`, {
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
      "creationDate": "2026-05-07T12:00:00.000Z",
      "creatorId": "string",
      "ID": "string",
      "lastUpdate": "2026-05-07T12:00:00.000Z",
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `creationDate` | date |  |
| `creatorId` | string |  |
| `ID` | string |  |
| `lastUpdate` | date |  |
| `message` | string |  |

## Native endpoint

Through the native Cliengo API, this operation is `GET /contacts/:contactId/notes` (base URL `https://api.cliengo.com/1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contact-notes.md) for the provider-specific parameters and requirements.

