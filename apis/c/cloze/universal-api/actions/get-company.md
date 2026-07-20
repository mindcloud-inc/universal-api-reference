# Cloze: Get Company

Retrieves a company from Cloze.

```
GET https://connect.mindcloud.co/v1/universal/cloze/latest/actions/get-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloze `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloze/latest/actions/get-company?connectionId=$CONNECTION_ID&uniqueid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "uniqueid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloze/latest/actions/get-company?${params}`, {
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
| `uniqueid` | string | yes | Company unique identifier such as domain name, email address, phone number, or social identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "company": {
        "assignee": "string",
        "description": "string",
        "direct": "string",
        "name": "Ava Chen",
        "segment": "string",
        "stage": "string"
      },
      "errorcode": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `company` | object | Returned company record |
| `company.assignee` | string | Assignee email |
| `company.description` | string | Company description |
| `company.direct` | string | Direct identifier |
| `company.name` | string | Company name |
| `company.segment` | string | Segment |
| `company.stage` | string | Stage |
| `errorcode` | number | Error code. 0 means success |

## Native endpoint

Through the native Cloze API, this operation is `GET /v1/companies/get` (base URL `https://api.cloze.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-company.md) for the provider-specific parameters and requirements.

