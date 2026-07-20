# Cloze: Update Person

Updates a person in Cloze.

```
PUT https://connect.mindcloud.co/v1/universal/cloze/latest/actions/update-person
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloze `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/cloze/latest/actions/update-person" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cloze/latest/actions/update-person', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `direct` | string | no | Direct identifier for the person to update. |
| `emails[]` | array<object> | no | Email addresses for the person. |
| `emails[].value` | string | no | Email address value. |
| `stage` | list<string> | no | Stage of the person. One of: `current`, `future`, `lead`, `out`, `past`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "errorcode": 1,
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `errorcode` | number | Error code. 0 means success |
| `message` | string | If an error occurs, this is the human readable description |

## Native endpoint

Through the native Cloze API, this operation is `POST /v1/people/update` (base URL `https://api.cloze.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-person.md) for the provider-specific parameters and requirements.

