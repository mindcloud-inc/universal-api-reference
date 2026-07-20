# Postalytics: Get Suppression List Contact

Retrieves a Postalytics suppression-list contact.

```
GET https://connect.mindcloud.co/v1/universal/postalytics/latest/actions/get-suppression-list-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Postalytics `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/postalytics/latest/actions/get-suppression-list-contact?connectionId=$CONNECTION_ID&listId=1&contactId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "listId": "1",
  "contactId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/postalytics/latest/actions/get-suppression-list-contact?${params}`, {
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
| `listId` | number | yes | Suppression list ID. |
| `contactId` | number | yes | Suppression contact ID. |
| `offset` | number | no | Starting offset. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ContactDetails": [
        {}
      ],
      "ListDetails": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ContactDetails` | array<object> | Matching suppression-list contact records. |
| `ListDetails` | object | Suppression list metadata. |

## Native endpoint

Through the native Postalytics API, this operation is `GET /api/v1/lists/suppression/contacts/:listId/:contactId` (base URL `https://api.postalytics.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-suppression-list-contact.md) for the provider-specific parameters and requirements.

