# JustCall: Bulk Add Contacts to Blacklist

Adds contacts to the JustCall blacklist.

```
POST https://connect.mindcloud.co/v1/universal/justCall/latest/actions/bulk-add-contacts-to-blacklist
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a JustCall `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/justCall/latest/actions/bulk-add-contacts-to-blacklist" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "addTo[]": [
    "string"
  ],
  "contactNumbers[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/justCall/latest/actions/bulk-add-contacts-to-blacklist', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "addTo[]": ["string"],
    "contactNumbers[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `addTo[]` | array<string> | yes | Status lists to add these contacts to. |
| `contactNumbers[]` | array<string> | yes | Contact numbers to blacklist. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `status` | string |  |

## Native endpoint

Through the native JustCall API, this operation is `POST /v2.1/contacts/bulk-add/blacklist` (base URL `https://api.justcall.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/bulk-add-contacts-to-blacklist.md) for the provider-specific parameters and requirements.

