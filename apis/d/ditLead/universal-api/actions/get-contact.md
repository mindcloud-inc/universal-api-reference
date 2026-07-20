# DitLead: Get Contact



```
GET https://connect.mindcloud.co/v1/universal/ditLead/latest/actions/get-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DitLead `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ditLead/latest/actions/get-contact?connectionId=$CONNECTION_ID&contactId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contactId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ditLead/latest/actions/get-contact?${params}`, {
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
| `contactId` | string | yes | Public ID of the contact. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "_id": "string",
        "addedVia": "string",
        "attributes": {},
        "campaignsParticipated": [
          "string"
        ],
        "emails": [
          {}
        ],
        "list": [
          "string"
        ],
        "publicId": "string"
      },
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data._id` | string |  |
| `data.addedVia` | string |  |
| `data.attributes` | object |  |
| `data.campaignsParticipated` | array<string> |  |
| `data.emails` | array<object> |  |
| `data.list` | array<string> |  |
| `data.publicId` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native DitLead API, this operation is `GET /v1/contact/{contactId}` (base URL `https://api.ditlead.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact.md) for the provider-specific parameters and requirements.

