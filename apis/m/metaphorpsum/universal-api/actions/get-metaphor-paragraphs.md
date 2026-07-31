# Metaphorpsum: Get Metaphor Paragraphs



```
GET https://connect.mindcloud.co/v1/universal/metaphorpsum/latest/actions/get-metaphor-paragraphs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Metaphorpsum `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/metaphorpsum/latest/actions/get-metaphor-paragraphs?connectionId=$CONNECTION_ID&paragraphCount=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "paragraphCount": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/metaphorpsum/latest/actions/get-metaphor-paragraphs?${params}`, {
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
| `paragraphCount` | number | yes | Number of paragraphs to generate (1–20). |

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

Through the native Metaphorpsum API, this operation is `GET /paragraphs/:paragraphCount?format=json` (base URL `https://lorem.casjay.coffee`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-metaphor-paragraphs.md) for the provider-specific parameters and requirements.

