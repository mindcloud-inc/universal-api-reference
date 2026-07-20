# Cloze: Create Person

Creates a person in Cloze.

```
POST https://connect.mindcloud.co/v1/universal/cloze/latest/actions/create-person
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloze `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cloze/latest/actions/create-person" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cloze/latest/actions/create-person', {
  method: 'POST',
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
| `dryrun` | boolean | no | Run validation without creating or updating the record |
| `emails[]` | array<object> | no | Array of email addresses |
| `emails[].preferred` | boolean | no | Make this the preferred email address |
| `emails[].type` | list<string> | no | Alternative to work or home fields when submitting records to Cloze One of: `bulk`, `home`, `work`. |
| `emails[].value` | string | no | The email address |
| `emails[].work` | boolean | no | Whether this is a work address |
| `first` | string | no | First name of the person |
| `last` | string | no | Last name of the person |
| `name` | string | no | Full name of the person |
| `segment` | string | no | Segment of the person |
| `stage` | list<string> | no | Stage of the person One of: `current`, `future`, `lead`, `out`, `past`. |

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

Through the native Cloze API, this operation is `POST /v1/people/create` (base URL `https://api.cloze.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-person.md) for the provider-specific parameters and requirements.

