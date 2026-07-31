# Yes/No: Get Answer



```
GET https://connect.mindcloud.co/v1/universal/yesNo/latest/actions/get-answer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Yes/No `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/yesNo/latest/actions/get-answer?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/yesNo/latest/actions/get-answer?${params}`, {
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
| `force` | list<string> | no | Optionally force the response to yes, no, or maybe. One of: `maybe`, `no`, `yes`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "answer": "string",
      "forced": true,
      "image": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `answer` | string | Decision answer: yes, no, or maybe. |
| `forced` | boolean | Whether an answer was forced. |
| `image` | string | Provider GIF image URL. |

## Native endpoint

Through the native Yes/No API, this operation is `GET /api` (base URL `https://yesno.wtf`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-answer.md) for the provider-specific parameters and requirements.

