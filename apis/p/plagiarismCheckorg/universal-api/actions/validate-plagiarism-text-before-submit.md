# PlagiarismCheck.org: Validate Plagiarism Text Before Submit



```
GET https://connect.mindcloud.co/v1/universal/plagiarismCheckorg/latest/actions/validate-plagiarism-text-before-submit
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PlagiarismCheck.org `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/plagiarismCheckorg/latest/actions/validate-plagiarism-text-before-submit?connectionId=$CONNECTION_ID&text=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "text": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/plagiarismCheckorg/latest/actions/validate-plagiarism-text-before-submit?${params}`, {
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
| `text` | string | yes | Plain text content to validate before submitting a plagiarism check. The official docs require at least 80 characters. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "hash": "string",
      "pages": 1,
      "success": true,
      "warning": "string",
      "words": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `hash` | string |  |
| `pages` | number |  |
| `success` | boolean |  |
| `warning` | string |  |
| `words` | number |  |

## Native endpoint

Through the native PlagiarismCheck.org API, this operation is `POST /api/v1/text/validate` (base URL `https://plagiarismcheck.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-plagiarism-text-before-submit.md) for the provider-specific parameters and requirements.

