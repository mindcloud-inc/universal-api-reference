# Cloze: Get Person

Retrieves a person from Cloze.

```
GET https://connect.mindcloud.co/v1/universal/cloze/latest/actions/get-person
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloze `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloze/latest/actions/get-person?connectionId=$CONNECTION_ID&uniqueid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "uniqueid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloze/latest/actions/get-person?${params}`, {
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
| `team` | boolean | no | Retrieve the team relation instead of the local relation. |
| `uniqueid` | string | yes | Person unique identifier such as email address, mobile phone number, or social identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "errorcode": 1,
      "person": {
        "assignee": "string",
        "direct": "string",
        "first": "string",
        "last": "string",
        "name": "Ava Chen",
        "segment": "string",
        "stage": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `errorcode` | number | Error code. 0 means success |
| `person` | object | Returned person record |
| `person.assignee` | string | Assignee email |
| `person.direct` | string | Direct identifier |
| `person.first` | string | First name |
| `person.last` | string | Last name |
| `person.name` | string | Full name |
| `person.segment` | string | Segment |
| `person.stage` | string | Stage |

## Native endpoint

Through the native Cloze API, this operation is `GET /v1/people/get` (base URL `https://api.cloze.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-person.md) for the provider-specific parameters and requirements.

