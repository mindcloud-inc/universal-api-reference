# Veracity Learning: Get Agent

Retrieves a Person Object for an agent from Veracity Learning.

```
GET https://connect.mindcloud.co/v1/universal/veracityLearning/latest/actions/get-agent
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Veracity Learning `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/veracityLearning/latest/actions/get-agent?connectionId=$CONNECTION_ID&agent=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "agent": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/veracityLearning/latest/actions/get-agent?${params}`, {
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
| `agent` | object | yes | Agent object used to fetch the expanded person record |

## Response

```json
{
  "success": true,
  "data": [
    {
      "account": [
        {}
      ],
      "mbox": [
        "string"
      ],
      "mboxSha1sum": [
        "string"
      ],
      "name": [
        "Ava Chen"
      ],
      "objectType": "string",
      "openid": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account` | array<object> | Account identifiers known for the person |
| `mbox` | array<string> | Email identifiers known for the person |
| `mboxSha1sum` | array<string> | SHA1 email identifiers known for the person |
| `name` | array<string> | Names associated with the person |
| `objectType` | string | xAPI object type for the returned agent person |
| `openid` | array<string> | OpenID identifiers known for the person |

## Native endpoint

Through the native Veracity Learning API, this operation is `GET /agents` (base URL `https://sample-lrs-rafehwe.lrs.io/xapi`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-agent.md) for the provider-specific parameters and requirements.

