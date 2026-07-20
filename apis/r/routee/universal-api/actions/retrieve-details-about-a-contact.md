# Routee: Retrieve details about a contact

Retrieves details about a contact from Routee.

```
GET https://connect.mindcloud.co/v1/universal/routee/latest/actions/retrieve-details-about-a-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Routee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/routee/latest/actions/retrieve-details-about-a-contact?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/routee/latest/actions/retrieve-details-about-a-contact?${params}`, {
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
| `id` | string | yes | The id of the contact. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "blacklistedServices": [
        [
          "string"
        ]
      ],
      "country": "string",
      "firstName": "Ava",
      "groups": [
        [
          "string"
        ]
      ],
      "id": "string",
      "labels": [
        [
          "string"
        ]
      ],
      "lastName": "Chen",
      "mobile": "string",
      "vip": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `blacklistedServices[]` | array |  |
| `country` | string |  |
| `firstName` | string |  |
| `groups[]` | array<string> |  |
| `id` | string |  |
| `labels[]` | array |  |
| `lastName` | string |  |
| `mobile` | string |  |
| `vip` | boolean |  |

## Native endpoint

Through the native Routee API, this operation is `GET /contacts/my/:id` (base URL `https://connect.routee.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-details-about-a-contact.md) for the provider-specific parameters and requirements.

