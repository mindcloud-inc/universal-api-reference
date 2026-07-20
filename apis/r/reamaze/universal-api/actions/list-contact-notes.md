# Reamaze: List Contact Notes



```
GET https://connect.mindcloud.co/v1/universal/reamaze/latest/actions/list-contact-notes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reamaze `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reamaze/latest/actions/list-contact-notes?connectionId=$CONNECTION_ID&contactIdentifier=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contactIdentifier": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/reamaze/latest/actions/list-contact-notes?${params}`, {
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
| `contactIdentifier` | string | yes | Path parameter for email\|phone. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "creator": {},
      "id": 1,
      "note": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `creator` | object |  |
| `id` | number |  |
| `note` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Reamaze API, this operation is `GET /contacts/:contactIdentifier/notes` (base URL `https://{{credentials.brand}}.reamaze.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contact-notes.md) for the provider-specific parameters and requirements.

