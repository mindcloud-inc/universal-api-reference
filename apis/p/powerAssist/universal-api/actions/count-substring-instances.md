# Power Assist: Count Substring Instances

Counts substring matches with Power Assist.

```
GET https://connect.mindcloud.co/v1/universal/powerAssist/latest/actions/count-substring-instances
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Power Assist `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/powerAssist/latest/actions/count-substring-instances?connectionId=$CONNECTION_ID&string=string&substring=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "string": "string",
  "substring": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/powerAssist/latest/actions/count-substring-instances?${params}`, {
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
| `string` | string | yes | The string to search within. |
| `substring` | string | yes | The substring to count. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `ignoreCase` | boolean | no | Whether matching should ignore letter case. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Result": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Result` | number | Number of substring instances. |

## Native endpoint

Through the native Power Assist API, this operation is `POST /api/string/countInstances` (base URL `https://power-assist.p.rapidapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/count-substring-instances.md) for the provider-specific parameters and requirements.

