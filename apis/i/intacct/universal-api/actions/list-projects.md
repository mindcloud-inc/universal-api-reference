# Sage Intacct: List Projects



```
GET https://connect.mindcloud.co/v1/universal/intacct/latest/actions/list-projects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sage Intacct `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/intacct/latest/actions/list-projects?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/intacct/latest/actions/list-projects?${params}`, {
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
| `filter[].filterfield` | string | no |  |
| `options[].caseinsensitive` | boolean | no |  |
| `filter[].filtertype` | list<string> | no |  |
| `filter[]` | array<object> | no |  |
| `filter[].filtervalue` | string | no |  |
| `docparid` | string | no |  |
| `entityID` | string | no |  |
| `options[]` | array | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "DESCRIPTION": {},
      "NAME": "Ava Chen",
      "PROJECTID": "string",
      "RECORDNO": "string",
      "STATUS": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `DESCRIPTION` | object |  |
| `NAME` | string |  |
| `PROJECTID` | string |  |
| `RECORDNO` | string |  |
| `STATUS` | string |  |

## Native endpoint

Through the native Sage Intacct API, this operation is `POST /` (base URL `https://api.intacct.com/ia/xml/xmlgw.phtml`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-projects.md) for the provider-specific parameters and requirements.

