# GoDial: Log Contact Disposition

Logs a disposition for a contact in GoDial.

```
PUT https://connect.mindcloud.co/v1/universal/goDial/latest/actions/contact-dispose
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoDial `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/goDial/latest/actions/contact-dispose" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "calledOn": "2026-05-07T12:00:00.000Z",
  "callerId": "string",
  "dispo": "string",
  "id": "string",
  "type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/goDial/latest/actions/contact-dispose', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "calledOn": "2026-05-07T12:00:00.000Z",
    "callerId": "string",
    "dispo": "string",
    "id": "string",
    "type": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `calledOn` | date | yes | Provide datetime when the call was made in ISO 8601 format with timezone offset. |
| `callerId` | string | yes | Provide the accountsId (member ID) of the agent/caller who made the call |
| `dispo` | string | yes | Provide disposition of the call made for the contact. Must be an UPPERCASE disposition value configured in your company. |
| `id` | string | yes | Contact ID. |
| `type` | string | yes | Mode of communication. Accepted values: Call, Sms, email |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean |  |

## Native endpoint

Through the native GoDial API, this operation is `POST /externals/contact/[:id]/dispose` (base URL `https://enterprise.godial.cc/meta/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/contact-dispose.md) for the provider-specific parameters and requirements.

