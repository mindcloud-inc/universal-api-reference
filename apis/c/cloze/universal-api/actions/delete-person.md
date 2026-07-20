# Cloze: Delete Person

Deletes a person from Cloze.

```
DELETE https://connect.mindcloud.co/v1/universal/cloze/latest/actions/delete-person
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloze `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/cloze/latest/actions/delete-person?connectionId=$CONNECTION_ID&uniqueid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "uniqueid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloze/latest/actions/delete-person?${params}`, {
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
| `team` | boolean | no | Delete the team relation instead of the local relation. |
| `uniqueid` | string | yes | Person unique identifier such as email address, mobile phone number, or social identifier. |

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

Through the native Cloze API, this operation is `DELETE /v1/people/delete` (base URL `https://api.cloze.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-person.md) for the provider-specific parameters and requirements.

