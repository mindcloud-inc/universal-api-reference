# Emelia: Add Contact To List

Adds a contact to a list in Emelia.

```
POST https://connect.mindcloud.co/v1/universal/emelia/latest/actions/add-contact-to-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Emelia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/emelia/latest/actions/add-contact-to-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contact": {
    "email": "apps+emelia-list-stage4@mindcloud.co",
    "lastName": "Cloud",
    "firstName": "Mind",
    "phoneNumber": "+15555550123"
  },
  "id": "69c6b32a8745944e0e345746"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/emelia/latest/actions/add-contact-to-list', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contact": {"email":"apps+emelia-list-stage4@mindcloud.co","lastName":"Cloud","firstName":"Mind","phoneNumber":"+15555550123"},
    "id": "69c6b32a8745944e0e345746"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contact` | string | yes | Contact payload JSON. Provide a JSON object string. Default: `{"email":"apps+emelia-list-stage4@mindcloud.co","lastName":"Cloud","firstName":"Mind","phoneNumber":"+15555550123"}`. |
| `id` | string | yes | List identifier Default: `69c6b32a8745944e0e345746`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "addContactsToListHook": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.addContactsToListHook` | string |  |

## Native endpoint

Through the native Emelia API, this operation is `POST /graphql` (base URL `https://graphql.emelia.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-contact-to-list.md) for the provider-specific parameters and requirements.

