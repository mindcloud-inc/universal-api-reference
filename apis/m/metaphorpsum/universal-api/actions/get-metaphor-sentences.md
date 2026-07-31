# Metaphorpsum: Get Metaphor Sentences



```
GET https://connect.mindcloud.co/v1/universal/metaphorpsum/latest/actions/get-metaphor-sentences
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Metaphorpsum `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/metaphorpsum/latest/actions/get-metaphor-sentences?connectionId=$CONNECTION_ID&sentenceCount=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sentenceCount": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/metaphorpsum/latest/actions/get-metaphor-sentences?${params}`, {
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
| `sentenceCount` | number | yes | Number of sentences to generate (1–50). |

## Response

```json
{
  "success": true,
  "data": [
    {
      "text": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `text` | string | Generated Metaphorpsum placeholder text. |

## Native endpoint

Through the native Metaphorpsum API, this operation is `GET /sentences/:sentenceCount?format=json` (base URL `https://lorem.casjay.coffee`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-metaphor-sentences.md) for the provider-specific parameters and requirements.

