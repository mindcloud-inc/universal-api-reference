# Alto: Get Contact Marketing Preferences

Retrieves contact marketing preferences from Alto by contact ID.

```
GET https://connect.mindcloud.co/v1/universal/alto/latest/actions/get-contact-marketing-preferences
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Alto `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/alto/latest/actions/get-contact-marketing-preferences?connectionId=$CONNECTION_ID&contactId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contactId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/alto/latest/actions/get-contact-marketing-preferences?${params}`, {
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
| `contactId` | string | yes | Unique Alto contact identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "actionedBy": "string",
      "contactId": 1,
      "dateActioned": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "optInStatus": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actionedBy` | string |  |
| `contactId` | number |  |
| `dateActioned` | date |  |
| `id` | number |  |
| `optInStatus` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Alto API, this operation is `GET /contacts/:contactId/preferences` (base URL `https://api.alto.zoopladev.co.uk`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact-marketing-preferences.md) for the provider-specific parameters and requirements.

