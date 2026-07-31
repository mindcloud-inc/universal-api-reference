# Bacon Ipsum: Generate Bacon Ipsum



```
GET https://connect.mindcloud.co/v1/universal/baconIpsum/latest/actions/generate-bacon-ipsum
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bacon Ipsum `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/baconIpsum/latest/actions/generate-bacon-ipsum?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/baconIpsum/latest/actions/generate-bacon-ipsum?${params}`, {
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
| `type` | string | no | Text type: all-meat or meat-and-filler. |
| `paras` | string | no | Number or range of paragraphs; defaults to 5 unless sentences is set. |
| `sentences` | string | no | Number of sentences; overrides paragraphs. |
| `startWithLorem` | string | no | Pass 1 to start the first paragraph with Bacon ipsum dolor sit amet. |

## Response

```json
{
  "success": true,
  "data": [
    {}
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `[]` | array<string> | Generated Bacon Ipsum paragraphs or sentences. |

## Native endpoint

Through the native Bacon Ipsum API, this operation is `GET /api/` (base URL `https://baconipsum.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-bacon-ipsum.md) for the provider-specific parameters and requirements.

